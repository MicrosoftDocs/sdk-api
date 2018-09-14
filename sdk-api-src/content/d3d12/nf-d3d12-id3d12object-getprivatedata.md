---
UID: NF:d3d12.ID3D12Object.GetPrivateData
title: ID3D12Object::GetPrivateData
author: windows-sdk-content
description: Gets application-defined data from a device object.
old-location: direct3d12\id3d12object_getprivatedata.htm
tech.root: direct3d12
ms.assetid: B2F1FFBE-1680-40D7-8B99-07FCA3F3EA0B
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetPrivateData, GetPrivateData method, GetPrivateData method,ID3D12Object interface, ID3D12Object interface,GetPrivateData method, ID3D12Object.GetPrivateData, ID3D12Object::GetPrivateData, d3d12/ID3D12Object::GetPrivateData, direct3d12.id3d12object_getprivatedata
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D12Object.GetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Object::GetPrivateData


## -description


Gets application-defined data from a device object.


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>

The <b>GUID</b> that is associated with the data.
          


### -param pDataSize [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that on input contains the size, in bytes, of the buffer that <i>pData</i> points to, and on output contains the size, in bytes, of the amount of data that <b>GetPrivateData</b> retrieved.
          


### -param pData [out, optional]

Type: <b>void*</b>

A pointer to a memory block that receives the data from the device object if <i>pDataSize</i> points to a value that specifies a buffer large enough to hold the data.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>
 

 

