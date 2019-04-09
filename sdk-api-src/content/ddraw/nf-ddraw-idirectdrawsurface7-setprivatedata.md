---
UID: NF:ddraw.IDirectDrawSurface7.SetPrivateData
title: IDirectDrawSurface7::SetPrivateData (ddraw.h)
author: windows-sdk-content
description: Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface.
old-location: directdraw\idirectdrawsurface7_setprivatedata.htm
tech.root: directdraw
ms.assetid: 822e4533-9073-4590-844e-8830110e4e33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "(none), DDSPD_IUNKNOWNPOINTER, DDSPD_VOLATILE, IDirectDrawSurface7 interface [DirectDraw],SetPrivateData method, IDirectDrawSurface7.SetPrivateData, IDirectDrawSurface7::SetPrivateData, SetPrivateData, SetPrivateData method [DirectDraw], SetPrivateData method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::SetPrivateData, directdraw.idirectdrawsurface7_setprivatedata"
ms.topic: method
req.header: ddraw.h
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawSurface7.SetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::SetPrivateData


## -description


Associates data with the surface that is intended for use by the application, not by DirectDraw. Data is passed by value, and multiple sets of data can be associated with a single surface.


## -parameters




### -param arg1 [in]

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to be set.


### -param arg2 [in]

A pointer to a buffer that contains the data to be associated with the surface.


### -param arg3 [in]

The size value of the buffer at <i>lpData</i>, in bytes.


### -param arg4 [in]

A value that can be set to one of the following flags. These flags describe the type of data being passed or request that the data be invalidated when the surface changes.



#### (none)

If no flags are specified, DirectDraw allocates memory to hold the data within the buffer and copies the data into the new buffer. The buffer allocated by DirectDraw is automatically freed, as appropriate.



#### DDSPD_IUNKNOWNPOINTER

The data at <i>lpData</i> is a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. DirectDraw automatically calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> method of this interface. When this data is no longer needed, DirectDraw automatically calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method of this interface.



#### DDSPD_VOLATILE

The buffer at <i>lpData</i> is only valid while the surface remains unchanged. If the surface's contents change, subsequent calls to the <a href="https://msdn.microsoft.com/f8c0c882-329f-4cce-8cd0-ff71c18b1716">IDirectDrawSurface7::GetPrivateData</a> method return DDERR_EXPIRED.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



DirectDraw does not manage the memory at <i>lpData</i>. If this buffer was dynamically allocated, the caller must free the memory.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetPrivateData</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

