-   Execution Instruction:
    
    -   Before Execution, Install the dependencies by running the following command on the terminal

        pip install requirements.txt

	-   For execution on the terminal,

        python run.py pointcloudfilename

        for e.g

        python run.py test_data/2d_pointcloud.txt

    -   You can also use the jupyter-notebook(run.ipynb) for testing, The name of test file has to be given manually in that case.

        OUTPUT:
            plot1
            plot2
            True
	
-   Some Pointer:

	-   Approach:

        In this Problem, I'm taking the point cloud as an input and estimating the ground plane in it and then if there are points which are not part of the plane, then the whole point cloud should not be the ground plane.
        
        threshold distance ratio is taken as 1
        maximum number of iteration for finding the plane is 50

        These two can be adjust according to the requirement.

    
    -   Supported file format for testfilename is .txt and .xyz

        -   I have used the RANSAC algorithm for ground plane estimation but there are so many other ways to detect it.

    
    -   The Problem was ambiguous so I've made the following assumptions:

        -   If the given point cloud has outliers(i.e they cannot lie on the plane or at a higher distance than the threshold value) then it is not the ground plane and vice versa.


	
