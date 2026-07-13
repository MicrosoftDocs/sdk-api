---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetManualStreamSelection
title: IWMReaderAdvanced::SetManualStreamSelection (wmsdkidl.h)
description: The SetManualStreamSelection method specifies whether stream selection is to be controlled manually.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetManualStreamSelection method","IWMReaderAdvanced.SetManualStreamSelection","IWMReaderAdvanced::SetManualStreamSelection","IWMReaderAdvancedSetManualStreamSelection","SetManualStreamSelection","SetManualStreamSelection method [windows Media Format]","SetManualStreamSelection method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setmanualstreamselection","wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection"]
old-location: wmformat\iwmreaderadvanced_setmanualstreamselection.htm
tech.root: wmformat
ms.assetid: 6950b26c-1763-4578-ab5c-0ea29d3d77f1
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetManualStreamSelection method, IWMReaderAdvanced.SetManualStreamSelection, IWMReaderAdvanced::SetManualStreamSelection, IWMReaderAdvancedSetManualStreamSelection, SetManualStreamSelection, SetManualStreamSelection method [windows Media Format], SetManualStreamSelection method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setmanualstreamselection, wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection
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
 - IWMReaderAdvanced::SetManualStreamSelection
 - wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection
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
 - IWMReaderAdvanced.SetManualStreamSelection
---

# IWMReaderAdvanced::SetManualStreamSelection


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetManualStreamSelection</b> method specifies whether stream selection is to be controlled manually. Stream selection applies to outputs associated with mutually exclusive streams. Under normal circumstances, the reader will select the most appropriate stream for an output at time of playback.

## -parameters

### -param fSelection [in]

Boolean value that is True if manual selection is specified.

## -returns

This method always returns S_OK.

## -remarks

When you call this method to enable manual stream selection, all streams in the file are selected. To select specific streams, pass an array of the desired stream numbers to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected">IWMReaderAdvanced::SetStreamsSelected</a> method.

When manual stream selection is enabled, you can manage the selected streams using <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected">GetStreamSelected</a> and <b>SetStreamsSelected</b>.

Stream numbers are in the range of 1 through 63.

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmanualstreamselection">IWMReaderAdvanced::GetManualStreamSelection</a>



<a href="/windows/desktop/wmformat/to-use-manual-stream-selection">To Use Manual Stream Selection</a>