---
UID: NF:wabapi.IWABObject.AllocateBuffer
title: IWABObject::AllocateBuffer
author: windows-sdk-content
description: Allocates memory for buffers that are passed to Windows Address Book (WAB) methods. The buffer must be freed with IWABObject::FreeBuffer, and may be reallocated with IWABObject::AllocateMore.
old-location: wab\_wab_IWABObject_AllocateBuffer.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\allocatebuffer.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AllocateBuffer, AllocateBuffer method [Windows Address Book], AllocateBuffer method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],AllocateBuffer method, IWABObject.AllocateBuffer, IWABObject::AllocateBuffer, _wab_IWABObject_AllocateBuffer, wab._wab_IWABObject_AllocateBuffer, wabapi/IWABObject::AllocateBuffer
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
 - IWABObject.AllocateBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IWABObject::AllocateBuffer


## -description


Allocates memory for buffers that are passed to 
		Windows Address Book (WAB) methods.  The buffer must be freed with 
		<a href="https://msdn.microsoft.com/ded42aaf-8ed0-4e21-9905-37629d2919a1">IWABObject::FreeBuffer</a>, and may be reallocated with 
		<a href="https://msdn.microsoft.com/f36171ce-7059-4a07-ad74-e3c092128821">IWABObject::AllocateMore</a>.


## -parameters




### -param cbSize

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies the size
				 in bytes of the buffer to be allocated.


### -param lppBuffer

Type: <b>LPVOID*</b>

Address of a pointer to the returned buffer.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the requested buffer was successfully 
			allocated.



