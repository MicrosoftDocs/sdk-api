---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# Matrix3x2F::Matrix3x2F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)


## -description


Instantiates a new instance of the <a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a> class that contains the specified values.


## -parameters




### -param m11




### -param m12




### -param m21




### -param m22




### -param m31




### -param m32






#### - _11

Type: <b>FLOAT</b>

The value in the first row and first column of the matrix.




#### - _12

Type: <b>FLOAT</b>

The value in the first row and second column of the matrix.




#### - _21

Type: <b>FLOAT</b>

The value in the second row and first column of the matrix.


#### - _22

Type: <b>FLOAT</b>

The value in the second row and second column of the matrix.


#### - _31

Type: <b>FLOAT</b>

The value in the third row and first column of the matrix.




#### - _32

Type: <b>FLOAT</b>

The value in the third row and second column of the matrix.




## -remarks



This method enables you to explicitly set the values of  matrix members. When using this method, ensure that each member represents an appropriate value for your transformation matrix. For example, to create the identity matrix, you must set <i>_11</i> and <i>_22</i> to 1, and the rest to 0. To create a translation matrix, you must set <i>_11</i> and <i>_22</i> to 1, <i>_12</i> and <i>_21</i> to 0, <i>_31</i> to the x displacement, and <i>_32</i> to the y displacement.

For convenience and accuracy, we recommended that whenever possible you use other helper functions, such as <a href="https://msdn.microsoft.com/c4596d43-fbc8-489e-a8fd-d33fb26461cc">Identity</a> and <a href="https://msdn.microsoft.com/eb289287-4f33-42cf-a306-120adda70371">Translation</a>, instead of this one.




## -see-also




<a href="https://msdn.microsoft.com/54b9e75c-6316-44d3-b725-2039f39eeda5">Matrix3x2F</a>
 

 

