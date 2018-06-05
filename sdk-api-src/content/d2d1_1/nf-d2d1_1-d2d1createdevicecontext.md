---
UID: NF:d2d1_1.D2D1CreateDeviceContext
title: D2D1CreateDeviceContext function
author: windows-sdk-content
description: Creates a new Direct2D device context associated with a DXGI surface.
old-location: direct2d\d2d1createdevicecontext.htm
old-project: Direct2D
ms.assetid: 0e56d057-20a5-47b7-aec9-63c8e31f349b
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: D2D1CreateDeviceContext, D2D1CreateDeviceContext function [Direct2D], d2d1_1/D2D1CreateDeviceContext, direct2d.d2d1createdevicecontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: D2D1_UNIT_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	d2d1.dll
api_name:
-	D2D1CreateDeviceContext
product: Windows
targetos: Windows
req.lib: 
req.dll: D2d1.dll
req.irql: 
---

# D2D1CreateDeviceContext function


## -description


Creates a new Direct2D device context associated with a DXGI surface. 


## -parameters




### -param dxgiSurface [in]

The DXGI surface the Direct2D device context is associated with.


### -param creationProperties [in, optional]

The properties to apply to the Direct2D device context.


### -param d2dDeviceContext [out]

When this function returns, contains the address of a pointer to a Direct2D device context.


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

This function will also create a new <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> that can be retrieved through <a href="https://msdn.microsoft.com/8c8664cb-d6be-41e0-8415-d60dcd46132a">ID2D1DeviceContext::GetDevice</a>.

The DXGI device will be specified implicitly through <i>dxgiSurface</i>.

If <i>creationProperties</i> are not specified, the Direct2D device will inherit its threading mode from the DXGI device implied by <i>dxgiSurface</i> and debug tracing will not be enabled.




## -see-also




<a href="https://msdn.microsoft.com/5ed3ec21-b609-41b6-9568-6ede460bc395">D2D1CreateDevice</a>



<a href="https://msdn.microsoft.com/0e56d057-20a5-47b7-aec9-63c8e31f349b">D2D1CreateDeviceContext</a>



<a href="https://msdn.microsoft.com/657439fe-dc17-42af-9e2c-2f3cb769a5a3">D2D1_CREATION_PROPERTIES</a>



<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>



<a href="https://msdn.microsoft.com/93afc187-d1ef-46f8-98b0-efe31345ae98">ID2D1Resource::GetFactory</a>
 

 

