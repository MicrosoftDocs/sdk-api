---
UID: NF:wmsdkidl.IWMAddressAccess.AddAccessEntry
title: IWMAddressAccess::AddAccessEntry (wmsdkidl.h)
description: The AddAccessEntry method adds an entry to the IP address access list.
helpviewer_keywords: ["AddAccessEntry","AddAccessEntry method [windows Media Format]","AddAccessEntry method [windows Media Format]","IWMAddressAccess interface","IWMAddressAccess interface [windows Media Format]","AddAccessEntry method","IWMAddressAccess.AddAccessEntry","IWMAddressAccess::AddAccessEntry","IWMAddressAccessAddAccessEntry","wmformat.iwmaddressaccess_addaccessentry","wmsdkidl/IWMAddressAccess::AddAccessEntry"]
old-location: wmformat\iwmaddressaccess_addaccessentry.htm
tech.root: wmformat
ms.assetid: 670bea6a-0370-4dc4-a2af-fcdbe2a6656a
ms.date: 4/26/2023
ms.keywords: AddAccessEntry, AddAccessEntry method [windows Media Format], AddAccessEntry method [windows Media Format],IWMAddressAccess interface, IWMAddressAccess interface [windows Media Format],AddAccessEntry method, IWMAddressAccess.AddAccessEntry, IWMAddressAccess::AddAccessEntry, IWMAddressAccessAddAccessEntry, wmformat.iwmaddressaccess_addaccessentry, wmsdkidl/IWMAddressAccess::AddAccessEntry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMAddressAccess::AddAccessEntry
 - wmsdkidl/IWMAddressAccess::AddAccessEntry
dev_langs:
 - c++
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
---

# IWMAddressAccess::AddAccessEntry


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddAccessEntry</b> method adds an entry to the IP address access list.

## -parameters

### -param aeType [in]

A member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wm_aetype">WM_AETYPE</a> enumeration specifying the access permissions (exclusion or inclusion).

### -param pAddrAccessEntry [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry">WM_ADDRESS_ACCESSENTRY</a> structure that specifies the IP address or range of addresses.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess Interface</a>