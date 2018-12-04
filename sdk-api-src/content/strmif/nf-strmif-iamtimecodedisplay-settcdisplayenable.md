---
UID: NF:strmif.IAMTimecodeDisplay.SetTCDisplayEnable
title: IAMTimecodeDisplay::SetTCDisplayEnable
author: windows-sdk-content
description: The SetTCDisplayEnable method enables or disables an external device's timecode character output generator.
old-location: dshow\iamtimecodedisplay_settcdisplayenable.htm
tech.root: DirectShow
ms.assetid: ae4eeeaa-1c73-4e3a-82b1-a073d9c7d667
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IAMTimecodeDisplay interface [DirectShow],SetTCDisplayEnable method, IAMTimecodeDisplay.SetTCDisplayEnable, IAMTimecodeDisplay::SetTCDisplayEnable, IAMTimecodeDisplaySetTCDisplayEnable, SetTCDisplayEnable, SetTCDisplayEnable method [DirectShow], SetTCDisplayEnable method [DirectShow],IAMTimecodeDisplay interface, dshow.iamtimecodedisplay_settcdisplayenable, strmif/IAMTimecodeDisplay::SetTCDisplayEnable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTimecodeDisplay.SetTCDisplayEnable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTimecodeDisplay::SetTCDisplayEnable


## -description



The <code>SetTCDisplayEnable</code> method enables or disables an external device's timecode character output generator.




## -parameters




### -param State [in]

Value specifying whether to enable or disable the timecode character output generator. Specify OATRUE to enable or OAFALSE to disable.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method is not intended for rendering characters inside a filter graph, it is purely intended for hardware displays. Ensure that your external timecode reader or generator has display capability before trying to use this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2edfc260-5bb6-475d-b8af-252e7c7a8552">IAMTimecodeDisplay Interface</a>



<a href="https://msdn.microsoft.com/fe8bac4d-a271-47b3-9737-f115429b50aa">IAMTimecodeDisplay::GetTCDisplayEnable</a>
 

 

