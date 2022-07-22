# NeuCodeFinder
A software tool for screening for the NeuCode signature in MS full scans

This project is to find neutron coded pairs in MS1 spectra, as an cooperation project with Dr. Chenxi Jia.
The peak detection algorithm and XIC construction algorithm are from our previously developed quantitative proteomics tool [PANDA](http://www.ncbi.nlm.nih.gov/pubmed/30816924)

## All the paramters were listed in the config file as follows:

//paramters for peak detection

MAX_CHARGE	5

SN_CUTOFF	1

PEAK_RINT_CUTOFF	0	//minimum peak relative intensity,default 0.

PEAK_INT_CUTOFF	1E5	//minimum peak absolute intensity

PEAK_TOLERANCE_PPM	10	//isotope peak mass tolerance: 10 ppm

//parameters in a neutron-coded pair

RATIO\_LIMIT\_LH	2	//maximum ratio cutoff for Heavy/Light or Light/Heavy in a neutron-coded pair

MIN\_MASS\_DIFF\_IN\_PAIR	5 //mDa

MAX\_MASS\_DIFF\_IN\_PAIR	100	//mDa

//paramters between neutron-coded pairs

MIN\_MASS\_DIFF\_BETWEEN\_PAIR	0	//mDa

MAX\_MASS\_DIFF\_BETWEEN_PAIR	5	//mDa

RT\_TOLERANCE	2	//max rt range when merging redundant ions, default +/-2min

ION\_TOLERANCE\_PPM	3 //precursor ion tolerance when merging redundant ions, default +/-3 ppm

MAX\_R\_NUM	5 //R number in a peptide sequence

PEAKPAIR\_LIMIT\_mDa	3	//the tolerance of the mass diff in a peak pair and the theoretical mass diff (42.3 mDa*Rum/charge)

//raw files (one file per line)

e:\task\task_NeutronCoding_JCX\data\raw_data\20160809_SILAC.raw
e:\task\task_NeutronCoding_JCX\data\raw_data\20160705_JCX_SLIAC_DDA_100per.raw 
