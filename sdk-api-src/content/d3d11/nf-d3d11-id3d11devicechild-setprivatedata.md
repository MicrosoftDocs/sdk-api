---
UID: NF:d3d11.ID3D11DeviceChild.SetPrivateData
title: ID3D11DeviceChild::SetPrivateData
author: windows-sdk-content
description: Set application-defined data to a device child and associate that data with an application-defined guid.
old-location: direct3d11\id3d11devicechild_setprivatedata.htm
tech.root: direct3d11
ms.assetid: 9b5d4c2f-fe1f-4131-9c04-2ea8fae6ee21
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 1f73a12c-1aa7-270f-b79f-ea48eb3ec3f5, ID3D11DeviceChild interface [Direct3D 11],SetPrivateData method, ID3D11DeviceChild.SetPrivateData, ID3D11DeviceChild::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 11], SetPrivateData method [Direct3D 11],ID3D11DeviceChild interface, d3d11/ID3D11DeviceChild::SetPrivateData, direct3d11.id3d11devicechild_setprivatedata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceChild.SetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceChild::SetPrivateData


## -description


Set application-defined data to a device child and associate that data with an application-defined guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the data.


### -param pData [in, optional]

Type: <b>const void*</b>

Pointer to the data to be stored with this device child. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the specified guid will be destroyed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The data stored in the device child with this method can be retrieved with <a href="https://msdn.microsoft.com/11729527-680e-4c70-a10f-278feab8362d">ID3D11DeviceChild::GetPrivateData</a>.

The <a href="https://msdn.microsoft.com/c545983c-5351-42a9-82e5-deea73aa035f">debug layer</a> reports memory leaks by outputting a list of object interface pointers along with their friendly names. The default friendly name is "&lt;unnamed&gt;". You can set the friendly name so that you can determine if the corresponding object interface pointer caused the leak. To set the friendly name, use the <b>SetPrivateData</b> method and the <b>WKPDID_D3DDebugObjectName</b> GUID that is in D3Dcommon.h. For example, to give pContext a friendly name of <i>My name</i>, use the following code:

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



## -see-also




<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

