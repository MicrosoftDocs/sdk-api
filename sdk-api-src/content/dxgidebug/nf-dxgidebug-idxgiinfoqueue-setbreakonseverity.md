---
UID: NF:dxgidebug.IDXGIInfoQueue.SetBreakOnSeverity
title: IDXGIInfoQueue::SetBreakOnSeverity
author: windows-sdk-content
description: Sets a message severity level to break on when a message with that severity level passes through the storage filter.
old-location: direct3ddxgi\idxgiinfoqueue_setbreakonseverity.htm
old-project: direct3ddxgi
ms.assetid: 3316A9E5-F65B-4162-9A5E-CDB5CD65FBF8
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IDXGIInfoQueue interface [DXGI],SetBreakOnSeverity method, IDXGIInfoQueue.SetBreakOnSeverity, IDXGIInfoQueue::SetBreakOnSeverity, SetBreakOnSeverity, SetBreakOnSeverity method [DXGI], SetBreakOnSeverity method [DXGI],IDXGIInfoQueue interface, direct3ddxgi.idxgiinfoqueue_setbreakonseverity, dxgidebug/IDXGIInfoQueue::SetBreakOnSeverity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.SetBreakOnSeverity
product: Windows
targetos: Windows
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIInfoQueue::SetBreakOnSeverity


## -description


Sets a message severity level to break on when a message with that severity level passes through the storage filter.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that sets the breaking condition.


### -param Severity [in]

A <a href="https://msdn.microsoft.com/99F9DDC8-5CCF-4991-94AD-0A399932F5B3">DXGI_INFO_QUEUE_MESSAGE_SEVERITY</a>-typed value that specifies the severity of the message.


### -param bEnable [in]

A Boolean value that specifies whether <b>SetBreakOnSeverity</b> turns on or off this breaking condition (<b>TRUE</b> for on, <b>FALSE</b> for off).


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

