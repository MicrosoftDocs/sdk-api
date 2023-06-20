---
UID: NF:wmsbuffer.INSSBuffer4.GetPropertyByIndex
title: INSSBuffer4::GetPropertyByIndex (wmsbuffer.h)
description: The GetPropertyByIndex method retrieves a buffer property, also called a data unit extension, that was set using INSSBuffer3::SetProperty.
helpviewer_keywords: ["GetPropertyByIndex","GetPropertyByIndex method [windows Media Format]","GetPropertyByIndex method [windows Media Format]","INSSBuffer4 interface","INSSBuffer4 interface [windows Media Format]","GetPropertyByIndex method","INSSBuffer4.GetPropertyByIndex","INSSBuffer4::GetPropertyByIndex","INSSBuffer4GetPropertyByIndex","wmformat.inssbuffer4_getpropertybyindex","wmsbuffer/INSSBuffer4::GetPropertyByIndex"]
old-location: wmformat\inssbuffer4_getpropertybyindex.htm
tech.root: wmformat
ms.assetid: 8812b7c9-610b-4c17-a274-55e043cfb091
ms.date: 4/26/2023
ms.keywords: GetPropertyByIndex, GetPropertyByIndex method [windows Media Format], GetPropertyByIndex method [windows Media Format],INSSBuffer4 interface, INSSBuffer4 interface [windows Media Format],GetPropertyByIndex method, INSSBuffer4.GetPropertyByIndex, INSSBuffer4::GetPropertyByIndex, INSSBuffer4GetPropertyByIndex, wmformat.inssbuffer4_getpropertybyindex, wmsbuffer/INSSBuffer4::GetPropertyByIndex
req.header: wmsbuffer.h
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
 - INSSBuffer4::GetPropertyByIndex
 - wmsbuffer/INSSBuffer4::GetPropertyByIndex
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
 - INSSBuffer4.GetPropertyByIndex
---

# INSSBuffer4::GetPropertyByIndex


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPropertyByIndex</b> method retrieves a buffer property, also called a data unit extension, that was set using <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty">INSSBuffer3::SetProperty</a>. This method differs from <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty">INSSBuffer3::GetProperty</a> in that, instead of accessing the property by name, it uses an index ranging from zero to one less than the total number of properties associated with the sample.

## -parameters

### -param dwBufferPropertyIndex [in]

<b>DWORD</b> containing the buffer property index. This value will be between zero and one less than the total number of properties associated with the sample. You can retrieve the total number of properties by calling <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer4-getpropertycount">INSSBuffer4::GetPropertyCount</a>.

### -param pguidBufferProperty [out]

Pointer to a GUID specifying the type of buffer property.

### -param pvBufferProperty [out]

Void pointer containing the value of the buffer property.

### -param pdwBufferPropertySize [in, out]

Pointer to a <b>DWORD</b> containing the size of the value pointed to by <i>pvBufferProperty</i>. If you set <i>pvBufferProperty</i> to <b>NULL</b>, this value will be set to the required size in bytes of the buffer needed to store the property value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4">INSSBuffer4 Interface</a>