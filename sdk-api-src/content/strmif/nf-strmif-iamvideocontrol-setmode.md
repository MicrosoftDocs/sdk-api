---
UID: NF:strmif.IAMVideoControl.SetMode
title: IAMVideoControl::SetMode
author: windows-sdk-content
description: The SetMode method sets the video control mode of operation.
old-location: dshow\iamvideocontrol_setmode.htm
old-project: DirectShow
ms.assetid: 09fe5d3f-41d8-4a60-a770-64c628a6b82d
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMVideoControl interface [DirectShow],SetMode method, IAMVideoControl.SetMode, IAMVideoControl::SetMode, IAMVideoControlSetMode, SetMode, SetMode method [DirectShow], SetMode method [DirectShow],IAMVideoControl interface, dshow.iamvideocontrol_setmode, strmif/IAMVideoControl::SetMode
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoControl.SetMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoControl::SetMode


## -description



The <code>SetMode</code> method sets the video control mode of operation.




## -parameters




### -param pPin [in]

Pointer to the pin to set the video control mode on.


### -param Mode [in]

Value specifying a combination of the flags from the <a href="https://msdn.microsoft.com/9d7feb46-fb07-46d8-a9a5-511578873cf3">VideoControlFlags</a> enumeration to set the video control mode.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Possible modes of operation include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd114977-c76c-4429-a835-98601b350a93">IAMVideoControl Interface</a>
 

 

