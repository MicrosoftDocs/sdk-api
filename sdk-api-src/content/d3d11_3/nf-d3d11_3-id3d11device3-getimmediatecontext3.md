---
UID: NF:d3d11_3.ID3D11Device3.GetImmediateContext3
title: ID3D11Device3::GetImmediateContext3
author: windows-sdk-content
description: Gets an immediate context, which can play back command lists.
old-location: direct3d11\id3d11device3_getimmediatecontext3.htm
tech.root: direct3d11
ms.assetid: E9E247C3-6326-46AC-A742-F5A4BE701B5B
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetImmediateContext3, GetImmediateContext3 method [Direct3D 11], GetImmediateContext3 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],GetImmediateContext3 method, ID3D11Device3.GetImmediateContext3, ID3D11Device3::GetImmediateContext3, d3d11_3/ID3D11Device3::GetImmediateContext3, direct3d11.id3d11device3_getimmediatecontext3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_3.h
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
 - ID3D11Device3.GetImmediateContext3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device3::GetImmediateContext3


## -description


Gets an immediate context, which can play back <a href="https://msdn.microsoft.com/en-us/library/Ff476885(v=VS.85).aspx">command lists</a>.
        


## -parameters




### -param ppImmediateContext [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn912875(v=VS.85).aspx">ID3D11DeviceContext3</a>**</b>

Upon completion of the method, the passed pointer to an <a href="https://msdn.microsoft.com/en-us/library/Dn912875(v=VS.85).aspx">ID3D11DeviceContext3</a> interface pointer is initialized.
          


## -returns



This method does not return a value.




## -remarks



The
          <b>GetImmediateContext3</b>method outputs an
          <a href="https://msdn.microsoft.com/en-us/library/Dn912875(v=VS.85).aspx">ID3D11DeviceContext3</a>object that represents an immediate context, which is used to perform rendering that you want immediately submitted to a device.
          For most apps, an immediate context is the primary object that is used to draw your scene.
        

The <b>GetImmediateContext3</b> method increments the reference count of the immediate context by one.
          Therefore, you must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the returned interface pointer when you are done with it to avoid a memory leak.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh404589(v=VS.85).aspx">ID3D11Device1::GetImmediateContext1</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn280496(v=VS.85).aspx">ID3D11Device2::GetImmediateContext2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn899218(v=VS.85).aspx">ID3D11Device3</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476529(v=VS.85).aspx">ID3D11Device::GetImmediateContext</a>
 

 

