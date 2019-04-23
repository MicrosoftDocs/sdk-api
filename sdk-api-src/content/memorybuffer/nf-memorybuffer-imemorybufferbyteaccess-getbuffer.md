---
UID: NF:memorybuffer.IMemoryBufferByteAccess.GetBuffer
title: IMemoryBufferByteAccess::GetBuffer (memorybuffer.h)
author: windows-sdk-content
description: Gets an IMemoryBuffer as an array of bytes.
old-location: winrt\imemorybufferbyteaccess_getbuffer.htm
tech.root: WinRT
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [Windows Runtime], GetBuffer method [Windows Runtime],IMemoryBufferByteAccess interface, IMemoryBufferByteAccess interface [Windows Runtime],GetBuffer method, IMemoryBufferByteAccess.GetBuffer, IMemoryBufferByteAccess::GetBuffer, memorybuffer/IMemoryBufferByteAccess::GetBuffer, winrt.imemorybufferbyteaccess_getbuffer
ms.topic: method
req.header: memorybuffer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - memorybuffer.h
api_name:
 - IMemoryBufferByteAccess.GetBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMemoryBufferByteAccess::GetBuffer


## -description


Gets an <a href="https://docs.microsoft.com/en-us/uwp/api/windows.foundation.imemorybuffer">IMemoryBuffer</a> as an array of bytes. 


## -parameters




### -param value [out]

A pointer to a byte array containing the buffer data.


### -param capacity [out]

The number of bytes in the returned array


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When <a href="https://docs.microsoft.com/en-us/uwp/api/windows.foundation.memorybuffer.close">MemoryBuffer::Close</a> is called, the code using this buffer should set the <i>value</i> pointer to null.




## -see-also




<a href="https://msdn.microsoft.com/F995FAC6-D873-41CC-9F92-A5A87BFE38FD">IMemoryBufferByteAccess</a>
 

 

