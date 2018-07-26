---
UID: NF:d3d10.ID3D10DeviceChild.SetPrivateDataInterface
title: ID3D10DeviceChild::SetPrivateDataInterface
author: windows-sdk-content
description: Associate an IUnknown-derived interface with this device child and associate that interface with an application-defined guid.
old-location: direct3d10\id3d10devicechild_setprivatedatainterface.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_setprivatedatainterface.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D10DeviceChild interface [Direct3D 10],SetPrivateDataInterface method, ID3D10DeviceChild.SetPrivateDataInterface, ID3D10DeviceChild::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Direct3D 10], SetPrivateDataInterface method [Direct3D 10],ID3D10DeviceChild interface, adb67004-d0c8-2bcc-dda9-a0dbc070dbda, d3d10/ID3D10DeviceChild::SetPrivateDataInterface, direct3d10.id3d10devicechild_setprivatedatainterface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10DeviceChild.SetPrivateDataInterface
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DeviceChild::SetPrivateDataInterface


## -description


Associate an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface with this device child and associate that interface with an application-defined guid.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the interface.


### -param pData [in]

Type: <b>const IUnknown*</b>

Pointer to an <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface to be associated with the device child.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



When this method is called ::addref() will be called on the <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a>-derived interface, and when the device child is detroyed ::release() will be called on the IUnknown-derived interface.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild Interface</a>
 

 

