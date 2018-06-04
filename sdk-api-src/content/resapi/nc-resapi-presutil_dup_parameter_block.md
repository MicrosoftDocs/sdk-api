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

# PRESUTIL_DUP_PARAMETER_BLOCK callback function


## -description


Performs a member-wise copy of the data from one  <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter block</a> to another.


## -parameters




### -param pOutParams [out]

Pointer to the duplicated parameter block.


### -param pInParams [in]

Pointer to the original parameter block.


### -param pPropertyTable [in]

Pointer to an array of  <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a> structures describing properties in the original parameter block.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, 
the function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<i>ResUtilDupParameterBlock</i> copies data only for parameter block members referenced in the <i>pPropertyTable</i> input parameter. If a variable in the input parameter block is a pointer, memory for the data is allocated with the function  <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>. You should deallocate this memory by calling either  <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> for each pointer variable in the output parameter block or  <a href="https://msdn.microsoft.com/2e884794-dbb7-47a8-8843-e9c030ce515d">ResUtilFreeParameterBlock</a>. Make sure that you deallocate memory whether  <i>ResUtilDupParameterBlock</i> succeeds or fails. For more information, see  <a href="https://msdn.microsoft.com/61bbda33-da5f-4826-b52a-e45252ac0374">Using Parameter Blocks</a> and  <a href="https://msdn.microsoft.com/f8f0297a-c050-41b9-a52f-a0265a18b87a">Using Lists and Tables</a>.




## -see-also




<a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>



<a href="https://msdn.microsoft.com/2e884794-dbb7-47a8-8843-e9c030ce515d">ResUtilFreeParameterBlock</a>
 

 

