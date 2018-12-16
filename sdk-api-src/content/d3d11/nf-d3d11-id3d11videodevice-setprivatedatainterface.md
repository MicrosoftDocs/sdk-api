---
UID: NF:d3d11.ID3D11VideoDevice.SetPrivateDataInterface
title: ID3D11VideoDevice::SetPrivateDataInterface
author: windows-sdk-content
description: Sets a private IUnknown pointer on the video device and associates that pointer with a GUID.
old-location: mf\id3d11videodevice_setprivatedatainterface.htm
tech.root: medfound
ms.assetid: E20FC248-92B2-4284-9EDC-9D5E6AB9506B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoDevice interface [Media Foundation],SetPrivateDataInterface method, ID3D11VideoDevice.SetPrivateDataInterface, ID3D11VideoDevice::SetPrivateDataInterface, SetPrivateDataInterface, SetPrivateDataInterface method [Media Foundation], SetPrivateDataInterface method [Media Foundation],ID3D11VideoDevice interface, d3d11/ID3D11VideoDevice::SetPrivateDataInterface, mf.id3d11videodevice_setprivatedatainterface
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoDevice.SetPrivateDataInterface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDevice::SetPrivateDataInterface


## -description


Sets a private <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer on the video device and associates that pointer with a GUID.



## -parameters




### -param guid [in]

The GUID associated with the pointer.


### -param pData [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

