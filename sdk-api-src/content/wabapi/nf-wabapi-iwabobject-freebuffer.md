---
UID: NF:wabapi.IWABObject.FreeBuffer
title: IWABObject::FreeBuffer
author: windows-sdk-content
description: Frees memory allocated with IWABObject::AllocateBuffer or any of the other Windows Address Book (WAB) methods.
old-location: wab\_wab_IWABObject_FreeBuffer.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\freebuffer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FreeBuffer, FreeBuffer method [Windows Address Book], FreeBuffer method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],FreeBuffer method, IWABObject.FreeBuffer, IWABObject::FreeBuffer, _wab_IWABObject_FreeBuffer, wab._wab_IWABObject_FreeBuffer, wabapi/IWABObject::FreeBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wabapi.h
req.include-header: 
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
req.lib: 
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.FreeBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wabapi.h
: 
- IWABObject.FreeBuffer
: 
req.product: Internet Explorer 4.0
---

# IWABObject::FreeBuffer


## -description


Frees memory allocated with 
		<a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">IWABObject::AllocateBuffer</a> or any of the other 
		Windows Address Book (WAB) methods.


## -parameters




### -param lpBuffer

Type: <b>LPVOID</b>

Pointer to the buffer to be freed.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the call succeeded 
			and freed the memory requested.



