---
UID: NF:d3d11.ID3D11Device.SetPrivateData
title: ID3D11Device::SetPrivateData
author: windows-sdk-content
description: Set data to a device and associate that data with a guid.
old-location: direct3d11\id3d11device_setprivatedata.htm
tech.root: direct3d11
ms.assetid: 0a8add57-b209-4096-9132-f3258469bdbd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11Device interface [Direct3D 11],SetPrivateData method, ID3D11Device.SetPrivateData, ID3D11Device::SetPrivateData, SetPrivateData, SetPrivateData method [Direct3D 11], SetPrivateData method [Direct3D 11],ID3D11Device interface, d3d11/ID3D11Device::SetPrivateData, direct3d11.id3d11device_setprivatedata, f1172c7e-62ba-f206-04b7-7dc3e29d9d16
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
 - ID3D11Device.SetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device::SetPrivateData


## -description


Set data to a device and associate that data with a guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the data.


### -param pData [in, optional]

Type: <b>const void*</b>

Pointer to the data to be stored with this device. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The data stored in the device with this method can be retrieved with <a href="https://msdn.microsoft.com/8aeb004e-4507-4bf4-bd79-2747feaf5e4d">ID3D11Device::GetPrivateData</a>.

The data and guid set with this method will typically be application-defined.

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




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

