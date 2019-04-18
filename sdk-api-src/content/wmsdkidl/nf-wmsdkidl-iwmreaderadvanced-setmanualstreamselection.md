---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetManualStreamSelection
title: IWMReaderAdvanced::SetManualStreamSelection (wmsdkidl.h)
author: windows-sdk-content
description: The SetManualStreamSelection method specifies whether stream selection is to be controlled manually.
old-location: wmformat\iwmreaderadvanced_setmanualstreamselection.htm
tech.root: wmformat
ms.assetid: 6950b26c-1763-4578-ab5c-0ea29d3d77f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetManualStreamSelection method, IWMReaderAdvanced.SetManualStreamSelection, IWMReaderAdvanced::SetManualStreamSelection, IWMReaderAdvancedSetManualStreamSelection, SetManualStreamSelection, SetManualStreamSelection method [windows Media Format], SetManualStreamSelection method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setmanualstreamselection, wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection
ms.topic: method
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
product: Windows
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



When you call this method to enable manual stream selection, all streams in the file are selected. To select specific streams, pass an array of the desired stream numbers to the <a href="https://msdn.microsoft.com/en-us/library/Dd743488(v=VS.85).aspx">IWMReaderAdvanced::SetStreamsSelected</a> method.

When manual stream selection is enabled, you can manage the selected streams using <a href="https://msdn.microsoft.com/en-us/library/Dd743478(v=VS.85).aspx">GetStreamSelected</a> and <b>SetStreamsSelected</b>.

Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743472(v=VS.85).aspx">IWMReaderAdvanced::GetManualStreamSelection</a>



<a href="https://msdn.microsoft.com/49ec283f-670a-4a0e-9477-c60a80919a1e">To Use Manual Stream Selection</a>
 

 

