#Solution File
class Node
	def initialize (datum,ref=nil)
		@datum=datum
		@ref=ref
	end

	def get_datum
		return @datum
	end

	def set_datum(newdatum)
		@datum=newdatum
	end

	def get_ref
		return @ref
	end

	def set_ref(newref)
		@ref=newref
	end
end

class Linkedlist
	def initialize
		@tam=0
		@header=nil
	end

	def add_element (value)
		@tam=@tam+1

		if @header==nil
			@header=Node.new(value)
		else
		actualnode=@header
		while actualnode.get_ref !=nil
			actualnode=actualnode.get_ref
		end
		actualnode.set_ref( Node.new(value) )
		end
	end

	def delete_element(datumtoeliminate)
		actualnode=@header
		if actualnode.get_datum==datumtoeliminate
			@header=@header.get_ref
		else
			actualnode=@header
			while(actualnode.get_ref !=nil) && ((actualnode.get_ref).get_datum !=datumtoeliminate)
				actualnode=actualnode.get_ref
			end
			if (actualnode !=nil) && (actualnode.get_ref !=nil)
				actualnode.set_ref( (actualnode.get_ref).get_ref )
			end
    		end
	end

	def print_list
		actualnode=@header
		complete_list=[]
		while actualnode.get_ref !=nil
			complete_list+=[actualnode.get_datum.to_s]
			actualnode=actualnode.get_ref
		end
		complete_list+=[actualnode.get_datum.to_s]
		printing = ""
		tamprinting=@tam-1
		for i in(0..tamprinting)
			printing=printing+complete_list[i].to_s
			if i <tamprinting
			printing+= ","
			end
		end
		puts printing
	end

	def get_tam
		return@tam
	end
end

list=Linkedlist.new
detention=nil
while detention !=-1
	z=gets.chomp
	if z.to_i==-1
		detention =-1
	else
	list.add_element(z)
	end
end

list.print_list

