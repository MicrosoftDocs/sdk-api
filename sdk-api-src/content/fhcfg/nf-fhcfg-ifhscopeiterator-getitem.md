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

# IFhScopeIterator::GetItem


## -description


Retrieves the current item in an inclusion or exclusion list.


## -parameters




### -param Item [out]

This parameter must be <b>NULL</b> on input. On output, it receives a pointer to a string that contains the current element of the list. This element is a library name or a folder name, depending on the parameters that were passed to the <a href="https://msdn.microsoft.com/DE137C08-923D-4ADC-8EBC-2F277F72CAE4">IFhConfigMgr::GetIncludeExcludeRules</a> method. The string is allocated by calling <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>. You must call <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the string when it is no longer needed.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



To move to the next item in the inclusion or exclusion list, call the <a href="https://msdn.microsoft.com/FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A">IFhScopeIterator::MoveToNextItem</a> method.




## -see-also




<a href="https://msdn.microsoft.com/E8F993BD-CB53-474A-926D-AED0F5A17073">IFhScopeIterator</a>



<a href="https://msdn.microsoft.com/FD8B5460-FBD7-47D3-ADB0-DB3D6AB5A51A">IFhScopeIterator::MoveToNextItem</a>
 

 

