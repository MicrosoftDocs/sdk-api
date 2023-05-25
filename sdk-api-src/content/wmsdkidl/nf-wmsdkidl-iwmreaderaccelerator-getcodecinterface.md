---
UID: NF:wmsdkidl.IWMReaderAccelerator.GetCodecInterface
title: IWMReaderAccelerator::GetCodecInterface (wmsdkidl.h)
description: The GetCodecInterface method is used to retrieve a pointer to the IWMCodecAMVideoAccelerator interface exposed on the decoder DMO.
helpviewer_keywords: ["GetCodecInterface","GetCodecInterface method [windows Media Format]","GetCodecInterface method [windows Media Format]","IWMReaderAccelerator interface","IWMReaderAccelerator interface [windows Media Format]","GetCodecInterface method","IWMReaderAccelerator.GetCodecInterface","IWMReaderAccelerator::GetCodecInterface","IWMReaderAcceleratorGetCodecInterface","wmformat.iwmreaderaccelerator_getcodecinterface","wmsdkidl/IWMReaderAccelerator::GetCodecInterface"]
old-location: wmformat\iwmreaderaccelerator_getcodecinterface.htm
tech.root: wmformat
ms.assetid: e38c02bb-335c-4f93-9e98-1a9dc65a37c5
ms.date: 4/26/2023
ms.keywords: GetCodecInterface, GetCodecInterface method [windows Media Format], GetCodecInterface method [windows Media Format],IWMReaderAccelerator interface, IWMReaderAccelerator interface [windows Media Format],GetCodecInterface method, IWMReaderAccelerator.GetCodecInterface, IWMReaderAccelerator::GetCodecInterface, IWMReaderAcceleratorGetCodecInterface, wmformat.iwmreaderaccelerator_getcodecinterface, wmsdkidl/IWMReaderAccelerator::GetCodecInterface
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
 - IWMReaderAccelerator::GetCodecInterface
 - wmsdkidl/IWMReaderAccelerator::GetCodecInterface
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
 - IWMReaderAccelerator.GetCodecInterface
---

# IWMReaderAccelerator::GetCodecInterface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecInterface</b> method is used to retrieve a pointer to the <a href="/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator">IWMCodecAMVideoAccelerator</a> interface exposed on the decoder <a href="/windows/desktop/wmformat/wmformat-glossary">DMO</a>.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param riid [in]

Reference to the IID of the interface to obtain. The value must be IID_IWMCodecAMVideoAccelerator.

### -param ppvCodecInterface [out]

Address of a pointer that receives the interface specified by <i>riid</i>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The WM Reader has no pointer to the codec.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator">IWMReaderAccelerator Interface</a>