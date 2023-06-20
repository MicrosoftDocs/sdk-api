---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetAllocateForOutput
title: IWMReaderAdvanced::SetAllocateForOutput (wmsdkidl.h)
description: The SetAllocateForOutput method specifies whether the reader allocates its own buffers for output samples or gets buffers from your application.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetAllocateForOutput method","IWMReaderAdvanced.SetAllocateForOutput","IWMReaderAdvanced::SetAllocateForOutput","IWMReaderAdvancedSetAllocateForOutput","SetAllocateForOutput","SetAllocateForOutput method [windows Media Format]","SetAllocateForOutput method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setallocateforoutput","wmsdkidl/IWMReaderAdvanced::SetAllocateForOutput"]
old-location: wmformat\iwmreaderadvanced_setallocateforoutput.htm
tech.root: wmformat
ms.assetid: fba76c75-6179-4e10-9a3c-8e604e392cca
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetAllocateForOutput method, IWMReaderAdvanced.SetAllocateForOutput, IWMReaderAdvanced::SetAllocateForOutput, IWMReaderAdvancedSetAllocateForOutput, SetAllocateForOutput, SetAllocateForOutput method [windows Media Format], SetAllocateForOutput method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setallocateforoutput, wmsdkidl/IWMReaderAdvanced::SetAllocateForOutput
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMReaderAdvanced::SetAllocateForOutput
 - wmsdkidl/IWMReaderAdvanced::SetAllocateForOutput
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
 - IWMReaderAdvanced.SetAllocateForOutput
---

# IWMReaderAdvanced::SetAllocateForOutput


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAllocateForOutput</b> method specifies whether the reader allocates its own buffers for output samples or gets buffers from your application.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.

### -param fAllocate [in]

Boolean value that is True if the reader gets buffers from your application.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

You can allocate your own buffers for file reading to reduce the overhead required by the reader object to allocate a new buffer for every sample. The reader object will make calls to the <b>IWMReaderCallbackAdvanced::AllocateForOutput</b> method.

If the application's callback implements the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex">IWMReaderAllocatorEx</a> interface, the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex">AllocateForOutputEx</a> method is called instead of <b>AllocateForOutput</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getallocateforoutput">IWMReaderAdvanced::GetAllocateForOutput</a>