---
UID: NF:d3d12.ID3D12Object.SetPrivateData
title: ID3D12Object::SetPrivateData method
author: windows-driver-content
description: Sets application-defined data to a device object and associates that data with an application-defined GUID.
old-location: direct3d12\id3d12object_setprivatedata.htm
old-project: direct3d12
ms.assetid: 1B3E8202-7CB3-4D9F-A1AE-70E66652773C
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D12Object, ID3D12Object interface, SetPrivateData method, ID3D12Object::SetPrivateData, SetPrivateData method, SetPrivateData method, ID3D12Object interface, SetPrivateData,ID3D12Object.SetPrivateData, d3d12/ID3D12Object::SetPrivateData, direct3d12.id3d12object_setprivatedata
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D12.dll
api_name:
-	ID3D12Object.SetPrivateData
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Object::SetPrivateData method


## -description



          Sets application-defined data to a device object and associates that data with an application-defined <b>GUID</b>.
        


## -parameters




### -param guid [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/cc237815(PROT.13).aspx">REFGUID</a></b>


            The <b>GUID</b> to associate with the data.
          


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            The size in bytes of the data.
          


### -param pData [in, optional]

Type: <b>const void*</b>


            A pointer to a memory block that contains the data to be stored with this device object. If <i>pData</i> is <b>NULL</b>, <i>DataSize</i> must also be 0, and any data that was previously associated with the <b>GUID</b> specified in <i>guid</i> will be destroyed.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks




        Rather than using the Direct3D 11 debug object naming scheme of calling <b>ID3D12Object::SetPrivateData</b> using <b>WKPDID_D3DDebugObjectName</b> with an ASCII name,
        call <a href="https://msdn.microsoft.com/A1DEEB16-BF75-4391-ADF0-AC22EECBC71A">ID3D12Object::SetName</a> with a UNICODE name.
      




## -see-also




<a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>
 

 

