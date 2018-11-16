---
UID: NF:wabapi.IWABObject.AllocateMore
title: IWABObject::AllocateMore
author: windows-sdk-content
description: Allocates a memory buffer that is linked to another buffer previously allocated with the IWABObject::AllocateBuffer method.
old-location: wab\_wab_IWABObject_AllocateMore.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\allocatemore.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AllocateMore, AllocateMore method [Windows Address Book], AllocateMore method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],AllocateMore method, IWABObject.AllocateMore, IWABObject::AllocateMore, _wab_IWABObject_AllocateMore, wab._wab_IWABObject_AllocateMore, wabapi/IWABObject::AllocateMore
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
 - IWABObject.AllocateMore
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
- IWABObject.AllocateMore
: 
req.product: Internet Explorer 4.0
---

# IWABObject::AllocateMore


## -description


Allocates a memory buffer that is linked to another buffer 
		previously allocated with the 
		<a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">IWABObject::AllocateBuffer</a> method.


## -parameters




### -param cbSize

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies 
				the size in bytes of the buffer to be allocated.


### -param lpObject

Type: <b>LPVOID</b>

Pointer to the existing buffer object allocated using 
				<a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">IWABObject::AllocateBuffer</a>.


### -param lppBuffer

Type: <b>LPVOID*</b>

Address of a pointer to the returned buffer. This buffer is linked to 
				<i>lpObject</i>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful.
			




## -remarks



It is only possible to release a buffer allocated with 
	<b>IWABObject::AllocateMore</b> by passing the buffer pointer 
	specified in the <i>lpObject</i> parameter to 
	<a href="https://msdn.microsoft.com/ded42aaf-8ed0-4e21-9905-37629d2919a1">IWABObject::FreeBuffer</a>. The link between the memory 
	buffers allocated with <a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">IWABObject::AllocateBuffer</a> and 
	<b>IWABObject::AllocateMore</b> enables 
	<b>IWABObject::FreeBuffer</b> to release both buffers 
	with a single call.



