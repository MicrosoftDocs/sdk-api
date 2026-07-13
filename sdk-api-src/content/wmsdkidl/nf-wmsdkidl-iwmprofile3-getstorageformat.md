---
UID: NF:wmsdkidl.IWMProfile3.GetStorageFormat
title: IWMProfile3::GetStorageFormat (wmsdkidl.h)
description: The GetStorageFormat method is not implemented.
helpviewer_keywords: ["GetStorageFormat","GetStorageFormat method [windows Media Format]","GetStorageFormat method [windows Media Format]","IWMProfile3 interface","IWMProfile3 interface [windows Media Format]","GetStorageFormat method","IWMProfile3.GetStorageFormat","IWMProfile3::GetStorageFormat","IWMProfile3GetStorageFormat","wmformat.iwmprofile3_getstorageformat","wmsdkidl/IWMProfile3::GetStorageFormat"]
old-location: wmformat\iwmprofile3_getstorageformat.htm
tech.root: wmformat
ms.assetid: 42aea1df-63cd-4eda-86c8-3cebe92d5c82
ms.date: 4/26/2023
ms.keywords: GetStorageFormat, GetStorageFormat method [windows Media Format], GetStorageFormat method [windows Media Format],IWMProfile3 interface, IWMProfile3 interface [windows Media Format],GetStorageFormat method, IWMProfile3.GetStorageFormat, IWMProfile3::GetStorageFormat, IWMProfile3GetStorageFormat, wmformat.iwmprofile3_getstorageformat, wmsdkidl/IWMProfile3::GetStorageFormat
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
 - IWMProfile3::GetStorageFormat
 - wmsdkidl/IWMProfile3::GetStorageFormat
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
 - IWMProfile3.GetStorageFormat
---

# IWMProfile3::GetStorageFormat


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStorageFormat</b> method is not implemented.

## -parameters

### -param pnStorageFormat [out]

Storage format.

## -returns

The method returns E_NOTIMPL.

## -remarks

To retrieve the storage format, use the <a href="/windows/desktop/wmformat/wm-containerformat">WM/ContainerFormat</a> attribute.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3 Interface</a>