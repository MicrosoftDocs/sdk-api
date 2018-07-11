---
UID: NF:d3d10.ID3D10DeviceChild.GetPrivateData
title: ID3D10DeviceChild::GetPrivateData
author: windows-sdk-content
description: Get application-defined data from a device child.
old-location: direct3d10\id3d10devicechild_getprivatedata.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10devicechild_getprivatedata.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 1156e7b1-1ba9-fab9-ab1a-7695c94278e9, GetPrivateData, GetPrivateData method [Direct3D 10], GetPrivateData method [Direct3D 10],ID3D10DeviceChild interface, ID3D10DeviceChild interface [Direct3D 10],GetPrivateData method, ID3D10DeviceChild.GetPrivateData, ID3D10DeviceChild::GetPrivateData, d3d10/ID3D10DeviceChild::GetPrivateData, direct3d10.id3d10devicechild_getprivatedata
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
 - ID3D10DeviceChild.GetPrivateData
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10DeviceChild::GetPrivateData


## -description


Get application-defined data from a device child.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

Guid associated with the data.


### -param pDataSize [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Size of the data.


### -param pData [out]

Type: <b>void*</b>

Pointer to the data stored with the device child. If pData is <b>NULL</b>, DataSize must also be 0, and any data previously associated with the guid will be destroyed.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



The data stored in the device child is set with <a href="https://msdn.microsoft.com/9eea3492-1f4f-49ea-88c8-064583ec6910">ID3D10DeviceChild::SetPrivateData</a>.




## -see-also




<a href="https://msdn.microsoft.com/64eff938-e130-48be-a45f-43f6c885b588">ID3D10DeviceChild Interface</a>
 

 

