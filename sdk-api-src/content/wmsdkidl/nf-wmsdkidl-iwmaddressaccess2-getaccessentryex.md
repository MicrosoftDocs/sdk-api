---
UID: NF:wmsdkidl.IWMAddressAccess2.GetAccessEntryEx
title: IWMAddressAccess2::GetAccessEntryEx (wmsdkidl.h)
description: The GetAccessEntryEx method retrieves an entry from the IP address access list.
helpviewer_keywords: ["GetAccessEntryEx","GetAccessEntryEx method [windows Media Format]","GetAccessEntryEx method [windows Media Format]","IWMAddressAccess2 interface","IWMAddressAccess2 interface [windows Media Format]","GetAccessEntryEx method","IWMAddressAccess2.GetAccessEntryEx","IWMAddressAccess2::GetAccessEntryEx","IWMAddressAccess2GetAccessEntryEx","wmformat.iwmaddressaccess2_getaccessentryex","wmsdkidl/IWMAddressAccess2::GetAccessEntryEx"]
old-location: wmformat\iwmaddressaccess2_getaccessentryex.htm
tech.root: wmformat
ms.assetid: 477e6b28-bfa0-4ce9-b2e0-eb51eaba6476
ms.date: 4/26/2023
ms.keywords: GetAccessEntryEx, GetAccessEntryEx method [windows Media Format], GetAccessEntryEx method [windows Media Format],IWMAddressAccess2 interface, IWMAddressAccess2 interface [windows Media Format],GetAccessEntryEx method, IWMAddressAccess2.GetAccessEntryEx, IWMAddressAccess2::GetAccessEntryEx, IWMAddressAccess2GetAccessEntryEx, wmformat.iwmaddressaccess2_getaccessentryex, wmsdkidl/IWMAddressAccess2::GetAccessEntryEx
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
 - IWMAddressAccess2::GetAccessEntryEx
 - wmsdkidl/IWMAddressAccess2::GetAccessEntryEx
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
 - IWMAddressAccess2.GetAccessEntryEx
---

# IWMAddressAccess2::GetAccessEntryEx


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAccessEntryEx</b> method retrieves an entry from the IP address access list.

## -parameters

### -param aeType [in]

A member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wm_aetype">WM_AETYPE</a> enumeration specifying the type of entry to retrieve (exclusion or inclusion).

### -param dwEntryNum [in]

Zero-based index of the entry. Use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmaddressaccess-getaccessentrycount">IWMAddressAccess::GetAccessEntryCount</a> method to get the number of entries.

### -param pbstrAddress [out]

Pointer to a variable that receives the IP address.

### -param pbstrMask [out]

Pointer to a variable that receives the bit mask.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about the meaning of the <i>pbstrAddress</i> and <i>pbstrMask</i> parameters, see <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmaddressaccess2-addaccessentryex">IWMAddressAccess2::AddAccessEntryEx</a>.

The caller must release the returned <b>BSTR</b> values, by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess2">IWMAddressAccess2 Interface</a>