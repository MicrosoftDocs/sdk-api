---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetManualStreamSelection
title: IWMReaderAdvanced::SetManualStreamSelection method
author: windows-driver-content
description: The SetManualStreamSelection method specifies whether stream selection is to be controlled manually.
old-location: wmformat\iwmreaderadvanced_setmanualstreamselection.htm
old-project: wmformat
ms.assetid: 6950b26c-1763-4578-ab5c-0ea29d3d77f1
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMReaderAdvanced, IWMReaderAdvanced interface [windows Media Format], SetManualStreamSelection method, IWMReaderAdvanced::SetManualStreamSelection, IWMReaderAdvancedSetManualStreamSelection, SetManualStreamSelection method [windows Media Format], SetManualStreamSelection method [windows Media Format], IWMReaderAdvanced interface, SetManualStreamSelection,IWMReaderAdvanced.SetManualStreamSelection, wmformat.iwmreaderadvanced_setmanualstreamselection, wmsdkidl/IWMReaderAdvanced::SetManualStreamSelection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced.SetManualStreamSelection
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::SetManualStreamSelection method


## -description



The <b>SetManualStreamSelection</b> method specifies whether stream selection is to be controlled manually. Stream selection applies to outputs associated with mutually exclusive streams. Under normal circumstances, the reader will select the most appropriate stream for an output at time of playback.




## -parameters




### -param fSelection [in]

Boolean value that is True if manual selection is specified.


## -returns



This method always returns S_OK.




## -remarks



When you call this method to enable manual stream selection, all streams in the file are selected. To select specific streams, pass an array of the desired stream numbers to the <a href="https://msdn.microsoft.com/921ab9fe-757f-4856-9fbc-b615bf92d90f">IWMReaderAdvanced::SetStreamsSelected</a> method.

When manual stream selection is enabled, you can manage the selected streams using <a href="https://msdn.microsoft.com/083fc743-79be-43c6-ac4b-458c74f42fa0">GetStreamSelected</a> and <b>SetStreamsSelected</b>.

Stream numbers are in the range of 1 through 63.




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/3205f508-a24b-4d24-a5e6-be16885e941b">IWMReaderAdvanced::GetManualStreamSelection</a>



<a href="https://msdn.microsoft.com/49ec283f-670a-4a0e-9477-c60a80919a1e">To Use Manual Stream Selection</a>
 

 

