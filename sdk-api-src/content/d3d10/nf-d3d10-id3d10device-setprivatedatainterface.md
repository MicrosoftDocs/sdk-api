---
UID: NF:d3d10.ID3D10Device.SetPrivateDataInterface
title: ID3D10Device::SetPrivateDataInterface
author: windows-sdk-content
description: Associate an IUnknown-derived interface with this device and associate that interface with an application-defined guid.
old-location: direct3d10\id3d10device_setprivatedatainterface.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_setprivatedatainterface.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10Device interface [Direct3D 10],SetPrivateDataInterface method, ID3D10Device.SetPrivateDataInterface, ID3D10Device::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 10], SetPrivateDataInterface method [Direct3D 10],ID3D10Device interface, ccad749b-460a-23ce-65bc-0e174fbf3d65, d3d10/ID3D10Device::SetPrivateDataInterface, direct3d10.id3d10device_setprivatedatainterface
ms.topic: method
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.SetPrivateDataInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Device::SetPrivateDataInterface


## -description


Associate an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface with this device and associate that interface with an application-defined guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the interface.


### -param pData [in]

Type: <b>const IUnknown*</b>

Pointer to an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface to be associated with the device.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



When this method is called ::addref() will be called on the IUnknown-derived interface, and when the device is detroyed ::release() will be called on the <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

