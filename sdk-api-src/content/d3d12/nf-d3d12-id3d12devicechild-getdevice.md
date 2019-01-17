---
UID: NF:d3d12.ID3D12DeviceChild.GetDevice
title: ID3D12DeviceChild::GetDevice
author: windows-sdk-content
description: Gets a pointer to the device that created this interface.
old-location: direct3d12\id3d12devicechild_getdevice.htm
tech.root: direct3d12
ms.assetid: FFF72E85-4382-420B-82C9-CE72B223F703
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDevice, GetDevice method, GetDevice method,ID3D12DeviceChild interface, ID3D12DeviceChild interface,GetDevice method, ID3D12DeviceChild.GetDevice, ID3D12DeviceChild::GetDevice, d3d12/ID3D12DeviceChild::GetDevice, direct3d12.id3d12devicechild_getdevice
ms.topic: method
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12DeviceChild.GetDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DeviceChild::GetDevice


## -description


Gets a pointer to the device that created this interface. 


## -parameters




### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the device interface.
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the device can be obtained by using the __uuidof() macro.
            For example, __uuidof(<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>) will get the <b>GUID</b> of the interface to a device.
          


### -param ppvDevice [out, optional]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a> interface for the device.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



Any returned interfaces have their reference count incremented by one, so be sure to call ::release() on the returned pointers before they are freed or else you will have a memory leak.
        


#### Examples

The <a href="https://msdn.microsoft.com/4C4475D4-534F-484F-8D60-9ACEA09AC109">D3D12Multithreading</a> sample uses <b>ID3D12DeviceChild::GetDevice</b> as follows:
        

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
</pre>
</td>
</tr>
</table></span></div>


Refer to the <a href="https://msdn.microsoft.com/C2323482-D06D-43B7-9BDE-BFB9A6A6B70D">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>
 

 

