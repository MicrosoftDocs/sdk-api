---
UID: NF:d3d12.ID3D12Object.GetPrivateData
title: ID3D12Object::GetPrivateData (d3d12.h)

description: Gets application-defined data from a device object.
old-location: direct3d12\id3d12object_getprivatedata.htm
tech.root: direct3d12
ms.assetid: B2F1FFBE-1680-40D7-8B99-07FCA3F3EA0B

ms.date: 12/05/2018
ms.keywords: GetPrivateData, GetPrivateData method, GetPrivateData method,ID3D12Object interface, ID3D12Object interface,GetPrivateData method, ID3D12Object.GetPrivateData, ID3D12Object::GetPrivateData, d3d12/ID3D12Object::GetPrivateData, direct3d12.id3d12object_getprivatedata
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12Object.GetPrivateData"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Object::GetPrivateData


## -description


Gets application-defined data from a device object.


## -parameters




### -param guid [in]

Type: <b><a href="https://docs.microsoft.com/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50">REFGUID</a></b>

The <b>GUID</b> that is associated with the data.
          


### -param pDataSize [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that on input contains the size, in bytes, of the buffer that <i>pData</i> points to, and on output contains the size, in bytes, of the amount of data that <b>GetPrivateData</b> retrieved.
          


### -param pData [out, optional]

Type: <b>void*</b>

A pointer to a memory block that receives the data from the device object if <i>pDataSize</i> points to a value that specifies a buffer large enough to hold the data.
          


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12object">ID3D12Object</a>
 

 

