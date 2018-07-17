---
UID: NF:dxgi.IDXGIObject.SetPrivateData
title: IDXGIObject::SetPrivateData
author: windows-sdk-content
description: Sets application-defined data to the object and associates that data with a GUID.
old-location: direct3ddxgi\idxgiobject_setprivatedata.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject_setprivatedata.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 5949633e-2d65-5d04-b6ba-29414dfded94, IDXGIObject interface [DXGI],SetPrivateData method, IDXGIObject.SetPrivateData, IDXGIObject::SetPrivateData, SetPrivateData, SetPrivateData method [DXGI], SetPrivateData method [DXGI],IDXGIObject interface, direct3ddxgi.idxgiobject_setprivatedata, dxgi/IDXGIObject::SetPrivateData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIObject.SetPrivateData
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIObject::SetPrivateData


## -description


Sets application-defined data to the object and associates that data with a GUID.


## -parameters




### -param Name [in]

Type: <b><a href="http://go.microsoft.com/?linkid=9742306">REFGUID</a></b>

A GUID that identifies the data. Use this GUID in a call to <a href="https://msdn.microsoft.com/library/Bb174543(v=VS.85).aspx">GetPrivateData</a> to get the data.


### -param DataSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The size of the object's data.


### -param pData [in]

Type: <b>const void*</b>

A pointer to the object's data.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> values.




## -remarks



<b>SetPrivateData</b> makes a copy of the specified data and stores it with the object.

Private data that <b>SetPrivateData</b> stores in the object occupies the same storage space as private data that is stored by associated Direct3D objects (for example, by a Microsoft Direct3D 11 device through <a href="https://msdn.microsoft.com/0a8add57-b209-4096-9132-f3258469bdbd">ID3D11Device::SetPrivateData</a> or by a Direct3D 11 child device through <a href="https://msdn.microsoft.com/9b5d4c2f-fe1f-4131-9c04-2ea8fae6ee21">ID3D11DeviceChild::SetPrivateData</a>).

The <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">debug layer</a> reports memory leaks by outputting a list of object interface pointers along with their friendly names. The default friendly name is "&lt;unnamed&gt;". You can set the friendly name so that you can determine if the corresponding object interface pointer caused the leak. To set the friendly name, use the <b>SetPrivateData</b> method and the well-known private data GUID (<b>WKPDID_D3DDebugObjectName</b>) that is in D3Dcommon.h. For example, to give pContext a friendly name of <i>My name</i>, use the following code:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
static const char c_szName[] = "My name";
hr = pContext-&gt;SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
</pre>
</td>
</tr>
</table></span></div>
You can use <b>WKPDID_D3DDebugObjectName</b> to track down memory leaks and understand performance characteristics of your applications. This information is reflected in the output of the <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">debug layer</a> that is related to memory leaks (<a href="https://msdn.microsoft.com/a4e5f3c1-8b67-488b-8476-464c5ea5abc6">ID3D11Debug::ReportLiveDeviceObjects</a>) and with the <a href="https://msdn.microsoft.com/2203D2D2-ECF6-4753-90FA-12A52678DFBB">event tracing</a> for Windows events that we've added to Windows 8.





## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb174541(v=VS.85).aspx">IDXGIObject</a>
 

 

