---
UID: NF:wmsdkidl.IWMAddressAccess2.AddAccessEntryEx
title: IWMAddressAccess2::AddAccessEntryEx
author: windows-sdk-content
description: The AddAccessEntryEx method adds an entry to the IP address access list.
old-location: wmformat\iwmaddressaccess2_addaccessentryex.htm
tech.root: wmformat
ms.assetid: 8125f716-0523-4042-a1f1-019445fb7de9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddAccessEntryEx, AddAccessEntryEx method [windows Media Format], AddAccessEntryEx method [windows Media Format],IWMAddressAccess2 interface, IWMAddressAccess2 interface [windows Media Format],AddAccessEntryEx method, IWMAddressAccess2.AddAccessEntryEx, IWMAddressAccess2::AddAccessEntryEx, IWMAddressAccess2AddAccessEntryEx, wmformat.iwmaddressaccess2_addaccessentryex, wmsdkidl/IWMAddressAccess2::AddAccessEntryEx
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
 - IWMAddressAccess2.AddAccessEntryEx
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
- IWMAddressAccess2.AddAccessEntryEx
: 
---

# IWMAddressAccess2::AddAccessEntryEx


## -description



The <b>AddAccessEntryEx</b> method adds an entry to the IP address access list.




## -parameters




### -param aeType [in]

A member of the <a href="https://msdn.microsoft.com/514e6745-c521-41bd-81c2-b6c24cfb0192">WM_AETYPE</a> enumeration specifying the specifying the access permissions (exclusion or inclusion).


### -param bstrAddress [in]

Specifies an IP address as a <b>BSTR</b>, using standard "dot" notation. Both IPv4 and IPv6 addresses are supported. For example, <code>206.73.118.1</code> is an IPv4 address and <code>fe80::201:3ff:fee8:5058</code> is an IPv6 address.


### -param bstrMask [in]

Bit mask that defines which bits in the IP address are matched against. For example, if the IP address is <code>206.73.118.1</code> and the mask is <code>255.255.255.0</code>, only the first 24 bits of the address are examined. Thus, any IP addresses in the range 206.73.118.<i>XXX</i> would match this entry.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/609a20a7-e1a3-4889-abf3-4a6defc7739a">IWMAddressAccess2 Interface</a>
 

 

