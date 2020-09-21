---
UID: NF:wmsdkidl.IWMAddressAccess.GetAccessEntryCount
title: IWMAddressAccess::GetAccessEntryCount (wmsdkidl.h)
description: The GetAccessEntryCount method retrieves the number of entries in the IP address access list.
helpviewer_keywords: ["GetAccessEntryCount","GetAccessEntryCount method [windows Media Format]","GetAccessEntryCount method [windows Media Format]","IWMAddressAccess interface","IWMAddressAccess interface [windows Media Format]","GetAccessEntryCount method","IWMAddressAccess.GetAccessEntryCount","IWMAddressAccess::GetAccessEntryCount","IWMAddressAccessGetAccessEntryCount","wmformat.iwmaddressaccess_getaccessentrycount","wmsdkidl/IWMAddressAccess::GetAccessEntryCount"]
old-location: wmformat\iwmaddressaccess_getaccessentrycount.htm
tech.root: wmformat
ms.assetid: 996d8a8a-887e-4e2f-b810-c57a4251f771
ms.date: 12/05/2018
ms.keywords: GetAccessEntryCount, GetAccessEntryCount method [windows Media Format], GetAccessEntryCount method [windows Media Format],IWMAddressAccess interface, IWMAddressAccess interface [windows Media Format],GetAccessEntryCount method, IWMAddressAccess.GetAccessEntryCount, IWMAddressAccess::GetAccessEntryCount, IWMAddressAccessGetAccessEntryCount, wmformat.iwmaddressaccess_getaccessentrycount, wmsdkidl/IWMAddressAccess::GetAccessEntryCount
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
 - IWMAddressAccess::GetAccessEntryCount
 - wmsdkidl/IWMAddressAccess::GetAccessEntryCount
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
 - IWMAddressAccess.GetAccessEntryCount
---

# IWMAddressAccess::GetAccessEntryCount


## -description

The <b>GetAccessEntryCount</b> method retrieves the number of entries in the IP address access list.

## -parameters

### -param aeType [in]

A member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wm_aetype">WM_AETYPE</a> enumeration specifying the type of entry (exclusion or inclusion).

### -param pcEntries [out]

Pointer to a variable that receives the number of entries of the type specified in <i>aeType</i>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmaddressaccess">IWMAddressAccess Interface</a>