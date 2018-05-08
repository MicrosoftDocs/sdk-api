---
UID: NF:dxgidebug.IDXGIInfoQueue.SetMuteDebugOutput
title: IDXGIInfoQueue::SetMuteDebugOutput
author: windows-driver-content
description: Turns the debug output on or off.
old-location: direct3ddxgi\idxgiinfoqueue_setmutedebugoutput.htm
old-project: direct3ddxgi
ms.assetid: F01E8BCC-CF82-4008-9829-C7EE4AD2973C
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetMuteDebugOutput method, IDXGIInfoQueue.SetMuteDebugOutput, IDXGIInfoQueue::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method [DXGI], SetMuteDebugOutput method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setmutedebugoutput, dxgidebug/IDXGIInfoQueue::SetMuteDebugOutput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGIDebug.dll
api_name:
-	IDXGIInfoQueue.SetMuteDebugOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::SetMuteDebugOutput


## -description


Turns the debug output on or off.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the mute status.


### -param bMute [in]

A Boolean value that specifies whether to turn the debug output on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).


## -returns



This method does not return a value.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

