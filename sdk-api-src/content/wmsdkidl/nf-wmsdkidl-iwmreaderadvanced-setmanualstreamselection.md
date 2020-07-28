---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetManualStreamSelection
title: IWMReaderAdvanced::SetManualStreamSelection (wmsdkidl.h)
description: The SetManualStreamSelection method specifies whether stream selection is to be controlled manually.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetManualStreamSelection method","IWMReaderAdvanced.SetManualStreamSelection","IWMReaderAdvanced::SetManualStreamSelection","IWMReaderAdvancedSetManualStreamSelection","SetManualStreamSelection","SetManualStreamSelection method [windows Media Format]","SetManualStreamSelection method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setmanualstreamselection","wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection"]
old-location: wmformat\iwmreaderadvanced_setmanualstreamselection.htm
tech.root: wmformat
ms.assetid: 6950b26c-1763-4578-ab5c-0ea29d3d77f1
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetManualStreamSelection method, IWMReaderAdvanced.SetManualStreamSelection, IWMReaderAdvanced::SetManualStreamSelection, IWMReaderAdvancedSetManualStreamSelection, SetManualStreamSelection, SetManualStreamSelection method [windows Media Format], SetManualStreamSelection method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setmanualstreamselection, wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection
f1_keywords:
- wmsdkidl/IWMReaderAdvanced.SetManualStreamSelection
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::SetManualStreamSelection


## -description



The <b>SetManualStreamSelection</b> method specifies whether stream selection is to be controlled manually. Stream selection applies to outputs associated with mutually exclusive streams. Under normal circumstances, the reader will select the most appropriate stream for an output at time of playback.




## -parameters




### -param fSelection [in]

Boolean value that is True if manual selection is specified.


## -returns



This method always returns S_OK.




## -remarks



When you call this method to enable manual stream selection, all streams in the file are selected. To select specific streams, pass an array of the desired stream numbers to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected">IWMReaderAdvanced::SetStreamsSelected</a> method.

When manual stream selection is enabled, you can manage the selected streams using <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected">GetStreamSelected</a> and <b>SetStreamsSelected</b>.

Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmanualstreamselection">IWMReaderAdvanced::GetManualStreamSelection</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/to-use-manual-stream-selection">To Use Manual Stream Selection</a>
 

 

