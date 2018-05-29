---
UID: NF:strmif.IAMTimecodeDisplay.GetTCDisplayEnable
title: IAMTimecodeDisplay::GetTCDisplayEnable
author: windows-sdk-content
description: The GetTCDisplayEnable method determines whether an external device's timecode character generator output is enabled or disabled.
old-location: dshow\iamtimecodedisplay_gettcdisplayenable.htm
old-project: DirectShow
ms.assetid: fe8bac4d-a271-47b3-9737-f115429b50aa
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetTCDisplayEnable, GetTCDisplayEnable method [DirectShow], GetTCDisplayEnable method [DirectShow],IAMTimecodeDisplay interface, IAMTimecodeDisplay interface [DirectShow],GetTCDisplayEnable method, IAMTimecodeDisplay.GetTCDisplayEnable, IAMTimecodeDisplay::GetTCDisplayEnable, IAMTimecodeDisplayGetTCDisplayEnable, dshow.iamtimecodedisplay_gettcdisplayenable, strmif/IAMTimecodeDisplay::GetTCDisplayEnable
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTimecodeDisplay.GetTCDisplayEnable
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTimecodeDisplay::GetTCDisplayEnable


## -description



The <code>GetTCDisplayEnable</code> method determines whether an external device's timecode character generator output is enabled or disabled.




## -parameters




### -param pState [out]

Pointer to a value indicating whether timecode character generator output is enabled. OATRUE indicates enabled; OAFALSE indicates disabled.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method is not intended for character rendering inside a filter graph, it is purely intended for hardware displays. Ensure that your external timecode reader or generator has display capability before trying to use this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2edfc260-5bb6-475d-b8af-252e7c7a8552">IAMTimecodeDisplay Interface</a>



<a href="https://msdn.microsoft.com/ae4eeeaa-1c73-4e3a-82b1-a073d9c7d667">IAMTimecodeDisplay::SetTCDisplayEnable</a>
 

 

