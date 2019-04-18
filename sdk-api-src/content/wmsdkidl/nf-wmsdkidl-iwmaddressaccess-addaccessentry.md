---
UID: NF:wmsdkidl.IWMAddressAccess.AddAccessEntry
title: IWMAddressAccess::AddAccessEntry (wmsdkidl.h)
author: windows-sdk-content
description: The AddAccessEntry method adds an entry to the IP address access list.
old-location: wmformat\iwmaddressaccess_addaccessentry.htm
tech.root: wmformat
ms.assetid: 670bea6a-0370-4dc4-a2af-fcdbe2a6656a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddAccessEntry, AddAccessEntry method [windows Media Format], AddAccessEntry method [windows Media Format],IWMAddressAccess interface, IWMAddressAccess interface [windows Media Format],AddAccessEntry method, IWMAddressAccess.AddAccessEntry, IWMAddressAccess::AddAccessEntry, IWMAddressAccessAddAccessEntry, wmformat.iwmaddressaccess_addaccessentry, wmsdkidl/IWMAddressAccess::AddAccessEntry
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
 - IWMAddressAccess.AddAccessEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMAddressAccess::AddAccessEntry


## -description



The <b>AddAccessEntry</b> method adds an entry to the IP address access list.




## -parameters




### -param aeType [in]

A member of the <a href="https://msdn.microsoft.com/en-us/library/Dd757889(v=VS.85).aspx">WM_AETYPE</a> enumeration specifying the access permissions (exclusion or inclusion).


### -param pAddrAccessEntry [in]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd757887(v=VS.85).aspx">WM_ADDRESS_ACCESSENTRY</a> structure that specifies the IP address or range of addresses.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd743279(v=VS.85).aspx">IWMAddressAccess Interface</a>
 

 

