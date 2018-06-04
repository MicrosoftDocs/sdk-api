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

# ReadFmtUserTypeStg function


## -description


The 
<b>ReadFmtUserTypeStg</b> function returns the clipboard format and user type previously saved with the 
<a href="https://msdn.microsoft.com/ef60493c-164e-4633-a248-05c4afade937">WriteFmtUserTypeStg</a> function.


## -parameters




### -param pstg

TBD


### -param pcf [out]

Pointer to where the clipboard format is to be written on return. It can be <b>NULL</b>, indicating the format is of no interest to the caller.


### -param lplpszUserType [out]

Address of <b>LPWSTR</b> pointer variable that receives a pointer to the null-terminated Unicode user-type string. The caller can specify <b>NULL</b> for this parameter, which indicates that the user type is of no interest. This function allocates memory for the string. The caller is responsible for freeing the memory with <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>.


#### - pStg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> interface on the storage object from which the information is to be read.


## -returns




						This function supports the standard return values E_FAIL, E_INVALIDARG, and E_OUTOFMEMORY, in addition to the following:

This function also returns any of the error values returned by the 
<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> method.




## -remarks



<b>ReadFmtUserTypeStg</b> returns the clipboard format and the user type string from the specified storage object. The 
<a href="https://msdn.microsoft.com/5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e">WriteClassStg</a> function must have been called before calling the 
<b>ReadFmtUserTypeStg</b> function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/ef60493c-164e-4633-a248-05c4afade937">WriteFmtUserTypeStg</a>
 

 

