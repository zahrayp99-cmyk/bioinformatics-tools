# bioinformatics-tools
dna_tools.py
def count_nucleotides(seq):
    return {
        "A": seq.count("A"),
        "T": seq.count("T"),
        "G": seq.count("G"),
        "C": seq.count("C")
    }

def gc_content(seq):
    g = seq.count("G")
    c = seq.count("C")
    return round(((g + c) / len(seq)) * 100, 2)

def reverse_complement(seq):
    complement = {"A":"T", "T":"A", "G":"C", "C":"G"}
    return "".join(complement[base] for base in reversed(seq))

if __name__ == "__main__":
    dna = input("Enter DNA sequence: ").upper()
    print("Nucleotide counts:", count_nucleotides(dna))
    print("GC content (%):", gc_content(dna))
    print("Reverse complement:", reverse_complement(dna))
