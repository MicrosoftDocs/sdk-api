---
UID: NF:dxgidebug.IDXGIInfoQueue.GetBreakOnID
title: IDXGIInfoQueue::GetBreakOnID
author: windows-sdk-content
description: Determines whether the break on a message identifier is turned on or off.
old-location: direct3ddxgi\idxgiinfoqueue_getbreakonid.htm
tech.root: direct3ddxgi
ms.assetid: A7DF79E0-137D-4CBD-AD03-B9BC4532D60F
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetBreakOnID, GetBreakOnID method [DXGI], GetBreakOnID method [DXGI],IDXGIInfoQueue interface, IDXGIInfoQueue interface [DXGI],GetBreakOnID method, IDXGIInfoQueue.GetBreakOnID, IDXGIInfoQueue::GetBreakOnID, direct3ddxgi.idxgiinfoqueue_getbreakonid, dxgidebug/IDXGIInfoQueue::GetBreakOnID
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIInfoQueue.GetBreakOnID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIInfoQueue::GetBreakOnID


## -description


Determines whether the break on a message identifier is turned on or off.


## -parameters




### -param Producer [in]

 A <a href="https://msdn.microsoft.com/85946D30-5E49-4E4B-AC25-394ABFF0DB11">DXGI_DEBUG_ID</a> value that identifies the entity that gets the breaking status.


### -param ID [in]

An integer value that specifies the identifier of the message.


## -returns



Returns a Boolean value that specifies whether this break on a message identifier is turned on or off (<b>TRUE</b> for on, <b>FALSE</b> for off).




## -remarks



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a>
 

 

