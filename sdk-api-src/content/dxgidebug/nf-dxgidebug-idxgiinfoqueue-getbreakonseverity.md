---
UID: NF:dxgidebug.IDXGIInfoQueue.GetBreakOnSeverity
title: IDXGIInfoQueue::GetBreakOnSeverity
author: windows-driver-content
description: Determines whether the break on a message severity level is turned on or off.
old-location: direct3ddxgi\idxgiinfoqueue_getbreakonseverity.htm
old-project: direct3ddxgi
ms.assetid: 0E03ABE8-02BC-4721-B92C-87DA5D52D0AD
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetBreakOnSeverity, GetBreakOnSeverity method [DXGI], GetBreakOnSeverity method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetBreakOnSeverity method, IDXGIInfoQueue.GetBreakOnSeverity, IDXGIInfoQueue::GetBreakOnSeverity, direct3ddxgi.idxgiinfoqueue_getbreakonseverity, dxgidebug/IDXGIInfoQueue::GetBreakOnSeverity
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
-	IDXGIInfoQueue.GetBreakOnSeverity
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::GetBreakOnSeverity


## -description


Determines whether the break on a message severity level is turned on or off.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the breaking status.


### -param Severity [in]

A <a href="https://msdn.microsoft.com/99F9DDC8-5CCF-4991-94AD-0A399932F5B3">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.


## -returns



Returns a Boolean value that specifies whether this severity of breaking condition is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

