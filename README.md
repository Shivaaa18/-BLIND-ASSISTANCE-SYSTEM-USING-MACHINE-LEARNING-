declare backbone map [7][7] feature map (256); //ResNet34

declare grid[49]:

declare anchor box[49] holds [shape][size]:

for i in 1 to 49.

anchor box[i] ([shape][size])= grid(shape,size):

declare obj_class;

declare location:

for i in 1 to 49:

if (degree(overlap) from anchor box[i] equals max(degree))

define obj_class;

define location:

obj_class-permute_from(anchor box.class);

location-permute_from(anchor box.loc);

permute from(anc_box_array.class(optional), loc(optional)):

for each element from anc_box_array:

get shape; //this parameter is to determine the shape of the anchor box

get size; //parameter to determine the size

get lighting: //parameter to determine the lighting

get pixel pattern; //parameter to determine the visible vs dark pixels

get aspect ratio; //parameter to determine the aspect ratio of the pixels

test cases:

if aspect ratio is like m:n where m>n then
