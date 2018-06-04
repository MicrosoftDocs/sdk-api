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

# IWMAddressAccess2::GetAccessEntryEx


## -description



The <b>GetAccessEntryEx</b> method retrieves an entry from the IP address access list.




## -parameters




### -param aeType [in]

A member of the <a href="https://msdn.microsoft.com/514e6745-c521-41bd-81c2-b6c24cfb0192">WM_AETYPE</a> enumeration specifying the type of entry to retrieve (exclusion or inclusion).


### -param dwEntryNum [in]

Zero-based index of the entry. Use the <a href="https://msdn.microsoft.com/996d8a8a-887e-4e2f-b810-c57a4251f771">IWMAddressAccess::GetAccessEntryCount</a> method to get the number of entries.


### -param pbstrAddress [out]

Pointer to a variable that receives the IP address.


### -param pbstrMask [out]

Pointer to a variable that receives the bit mask.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the meaning of the <i>pbstrAddress</i> and <i>pbstrMask</i> parameters, see <a href="https://msdn.microsoft.com/8125f716-0523-4042-a1f1-019445fb7de9">IWMAddressAccess2::AddAccessEntryEx</a>.

The caller must release the returned <b>BSTR</b> values, by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/609a20a7-e1a3-4889-abf3-4a6defc7739a">IWMAddressAccess2 Interface</a>
 

 

