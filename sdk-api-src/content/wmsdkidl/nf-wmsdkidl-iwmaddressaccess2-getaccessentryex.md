---
UID: NF:wmsdkidl.IWMAddressAccess2.GetAccessEntryEx
title: IWMAddressAccess2::GetAccessEntryEx
author: windows-sdk-content
description: The GetAccessEntryEx method retrieves an entry from the IP address access list.
old-location: wmformat\iwmaddressaccess2_getaccessentryex.htm
tech.root: wmformat
ms.assetid: 477e6b28-bfa0-4ce9-b2e0-eb51eaba6476
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetAccessEntryEx, GetAccessEntryEx method [windows Media Format], GetAccessEntryEx method [windows Media Format],IWMAddressAccess2 interface, IWMAddressAccess2 interface [windows Media Format],GetAccessEntryEx method, IWMAddressAccess2.GetAccessEntryEx, IWMAddressAccess2::GetAccessEntryEx, IWMAddressAccess2GetAccessEntryEx, wmformat.iwmaddressaccess2_getaccessentryex, wmsdkidl/IWMAddressAccess2::GetAccessEntryEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMAddressAccess2.GetAccessEntryEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMAddressAccess2.GetAccessEntryEx
: 
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
 

 

