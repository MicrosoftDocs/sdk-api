---
UID: NF:d2d1_1.D2D1CreateDevice
title: D2D1CreateDevice function
author: windows-sdk-content
description: Creates a new Direct2D device associated with the provided DXGI device.
old-location: direct2d\d2d1createdevice.htm
tech.root: direct2d
ms.assetid: 5ed3ec21-b609-41b6-9568-6ede460bc395
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1CreateDevice, D2D1CreateDevice function [Direct2D], d2d1_1/D2D1CreateDevice, direct2d.d2d1createdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d2d1.dll
api_name:
 - D2D1CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D2D1CreateDevice function


## -description


Creates a new Direct2D device associated with the provided DXGI device. 


## -parameters




### -param dxgiDevice [in]

The DXGI device the Direct2D device is associated with.


### -param creationProperties [in, optional]

The properties to apply to the Direct2D device.


### -param d2dDevice [out]

When this function returns, contains the address of a pointer to a Direct2D device.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>
 




## -remarks



This function will also create a new <a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a> that can be retrieved through <a href="https://msdn.microsoft.com/93afc187-d1ef-46f8-98b0-efe31345ae98">ID2D1Resource::GetFactory</a>.

If the creation properties are not specified, then <i>d2dDevice</i> will inherit its threading mode from <i>dxgiDevice</i> and debug tracing will not be enabled.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd368034(v=VS.85).aspx">D2D1CreateFactory</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404298(v=VS.85).aspx">D2D1_CREATION_PROPERTIES</a>



<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>



<a href="https://msdn.microsoft.com/93afc187-d1ef-46f8-98b0-efe31345ae98">ID2D1Resource::GetFactory</a>
 

 

