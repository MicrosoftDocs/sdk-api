---
UID: NF:wmsdkidl.IWMAddressAccess.GetAccessEntry
title: IWMAddressAccess::GetAccessEntry (wmsdkidl.h)
description: The GetAccessEntry method retrieves an entry from the IP address access list.
helpviewer_keywords: ["GetAccessEntry","GetAccessEntry method [windows Media Format]","GetAccessEntry method [windows Media Format]","IWMAddressAccess interface","IWMAddressAccess interface [windows Media Format]","GetAccessEntry method","IWMAddressAccess.GetAccessEntry","IWMAddressAccess::GetAccessEntry","IWMAddressAccessGetAccessEntry","wmformat.iwmaddressaccess_getaccessentry","wmsdkidl/IWMAddressAccess::GetAccessEntry"]
old-location: wmformat\iwmaddressaccess_getaccessentry.htm
tech.root: wmformat
ms.assetid: b01b921b-0bb8-447b-877c-8ac218422d36
ms.date: 4/26/2023
ms.keywords: GetAccessEntry, GetAccessEntry method [windows Media Format], GetAccessEntry method [windows Media Format],IWMAddressAccess interface, IWMAddressAccess interface [windows Media Format],GetAccessEntry method, IWMAddressAccess.GetAccessEntry, IWMAddressAccess::GetAccessEntry, IWMAddressAccessGetAccessEntry, wmformat.iwmaddressaccess_getaccessentry, wmsdkidl/IWMAddressAccess::GetAccessEntry
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
 - IWMAddressAccess::GetAccessEntry
 - wmsdkidl/IWMAddressAccess::GetAccessEntry
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
 - IWMAddressAccess.GetAccessEntry
---

# IWMAddressAccess::GetAccessEntry


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAccessEntry</b> method retrieves an entry from the IP address access list.

## -parameters

### -param aeType [in]

A member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wm_aetype">WM_AETYPE</a> enumeration specifying the type of entry to retrieve (exclusion or inclusion).

### -param dwEntryNum [in]

Specifies the zero-based index of the entry. Use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmaddressaccess-getaccessentrycount">IWMAddressAccess::GetAccessEntryCount</a> method to get the number of entries.

### -param pAddrAccessEntry [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry">WM_ADDRESS_ACCESSENTRY</a> structure that receives the access entry.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_INDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid index number.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess Interface</a>