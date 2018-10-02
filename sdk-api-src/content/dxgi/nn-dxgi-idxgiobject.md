---
UID: NN:dxgi.IDXGIObject
title: IDXGIObject
author: windows-sdk-content
description: An IDXGIObject interface is a base interface for all DXGI objects; IDXGIObject supports associating caller-defined (private data) with an object and retrieval of an interface to the parent object.
old-location: direct3ddxgi\idxgiobject.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDXGIObject, IDXGIObject interface [DXGI], IDXGIObject interface [DXGI],described, ae721ac9-3ed3-d7ef-07a7-3f3acbb19dcd, direct3ddxgi.idxgiobject, dxgi/IDXGIObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIObject interface


## -description


An <b>IDXGIObject</b> interface is a base interface for all DXGI objects;
        <b>IDXGIObject</b> supports associating caller-defined (private data) with an object and retrieval of an interface to the parent object.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGIObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174542(v=VS.85).aspx">GetParent</a>
</td>
<td align="left" width="63%">
Gets the parent of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174543(v=VS.85).aspx">GetPrivateData</a>
</td>
<td align="left" width="63%">
Get a pointer to the object's data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174544(v=VS.85).aspx">SetPrivateData</a>
</td>
<td align="left" width="63%">
Sets application-defined data to the object and associates that data with a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174545(v=VS.85).aspx">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Set an interface in the object's private data.

</td>
</tr>
</table> 


## -remarks



<b>IDXGIObject</b> implements base-class functionality for the following interfaces:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174535(v=VS.85).aspx">IDXGIFactory</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
</li>
</ul>
<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

