---
UID: NF:wabapi.IWABObject.AllocateMore
title: IWABObject::AllocateMore (wabapi.h)
description: Allocates a memory buffer that is linked to another buffer previously allocated with the IWABObject::AllocateBuffer method.
helpviewer_keywords: ["AllocateMore","AllocateMore method [Windows Address Book]","AllocateMore method [Windows Address Book]","IWABObject interface","IWABObject interface [Windows Address Book]","AllocateMore method","IWABObject.AllocateMore","IWABObject::AllocateMore","_wab_IWABObject_AllocateMore","wab._wab_IWABObject_AllocateMore","wabapi/IWABObject::AllocateMore"]
old-location: wab\_wab_IWABObject_AllocateMore.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\allocatemore.htm
ms.date: 12/05/2018
ms.keywords: AllocateMore, AllocateMore method [Windows Address Book], AllocateMore method [Windows Address Book],IWABObject interface, IWABObject interface [Windows Address Book],AllocateMore method, IWABObject.AllocateMore, IWABObject::AllocateMore, _wab_IWABObject_AllocateMore, wab._wab_IWABObject_AllocateMore, wabapi/IWABObject::AllocateMore
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IWABObject::AllocateMore
 - wabapi/IWABObject::AllocateMore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject.AllocateMore
---

# IWABObject::AllocateMore


## -description

Allocates a memory buffer that is linked to another buffer 
		previously allocated with the 
		<a href="/windows/desktop/api/wabapi/nf-wabapi-iwabobject-allocatebuffer">IWABObject::AllocateBuffer</a> method.

## -parameters

### -param cbSize

Type: <b>ULONG</b>

Value of type <b>ULONG</b> that specifies 
				the size in bytes of the buffer to be allocated.

### -param lpObject

Type: <b>LPVOID</b>

Pointer to the existing buffer object allocated using 
				<a href="/windows/desktop/api/wabapi/nf-wabapi-iwabobject-allocatebuffer">IWABObject::AllocateBuffer</a>.

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
	<a href="/windows/desktop/api/wabapi/nf-wabapi-iwabobject-freebuffer">IWABObject::FreeBuffer</a>. The link between the memory 
	buffers allocated with <a href="/windows/desktop/api/wabapi/nf-wabapi-iwabobject-allocatebuffer">IWABObject::AllocateBuffer</a> and 
	<b>IWABObject::AllocateMore</b> enables 
	<b>IWABObject::FreeBuffer</b> to release both buffers 
	with a single call.