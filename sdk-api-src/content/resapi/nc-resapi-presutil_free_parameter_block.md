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

# PRESUTIL_FREE_PARAMETER_BLOCK callback function


## -description


Deallocates memory that has been allocated for a  <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter block</a> by  <a href="https://msdn.microsoft.com/b05b5afe-7d4b-4a21-9f28-88d6effaf5af">ResUtilDupParameterBlock</a>.


## -parameters




### -param pOutParams [in, out]

Pointer to the parameter block to deallocate.


### -param pInParams [in]

Pointer to the parameter block to use as a reference.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing the properties in the input parameter block.


## -returns



This function has no return values.




## -remarks



The  <i>ResUtilFreeParameterBlock</i> utility function deallocates any memory allocated to each member of <i>pOutParams</i>, subject to the following limitations:

<ul>
<li>It will only deallocate memory for members referenced in the <i>pPropertyTable</i> input parameter.</li>
<li>It will not deallocate memory that is pointed to by any member of <i>pInParams</i>.</li>
</ul>
Do not use this function with parameter blocks that have not been allocated with  <a href="https://msdn.microsoft.com/b05b5afe-7d4b-4a21-9f28-88d6effaf5af">ResUtilDupParameterBlock</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/b05b5afe-7d4b-4a21-9f28-88d6effaf5af">ResUtilDupParameterBlock</a>
 

 

