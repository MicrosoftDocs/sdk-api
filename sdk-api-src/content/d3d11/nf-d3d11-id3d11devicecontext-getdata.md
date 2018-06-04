---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D11DeviceContext::GetData


## -description


Get data from the graphics processing unit (GPU) asynchronously.


## -parameters




### -param pAsync [in]

Type: <b><a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a> interface for the object about which <b>GetData</b> retrieves data.


### -param pData [out, optional]

Type: <b>void*</b>

Address of memory that will receive the data. If <b>NULL</b>, <b>GetData</b> will be used only to check status. The type of data output depends on the type of asynchronous interface.


### -param DataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of the data to retrieve or 0. Must be 0 when <i>pData</i> is <b>NULL</b>.


### -param GetDataFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional flags. Can be 0 or any combination of the flags enumerated by <a href="https://msdn.microsoft.com/e2e40719-58ff-4440-b162-34f5edee021d">D3D11_ASYNC_GETDATA_FLAG</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>. A return value of S_OK indicates that the data at <i>pData</i> is available for the calling application to access. A return value of S_FALSE indicates that the data is not yet available. If the data is not yet available, the application must call <b>GetData</b> until the data is available.




## -remarks



Queries in a deferred context are limited to predicated drawing. That is, you cannot call <b>ID3D11DeviceContext::GetData</b> on a deferred context to get data about a query; you can only call <b>GetData</b> on the immediate context to get data about a query. For predicated drawing, the results of a predication-type query are used by the GPU and not returned to an application. For more information about predication and predicated drawing, see <a href="https://msdn.microsoft.com/ceac248a-31c9-4e14-892f-f047e288daae">D3D11DeviceContext::SetPredication</a>.

<b>GetData</b> retrieves the data that the runtime collected between calls to <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> and <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a>.  Certain queries only require a call to <b>ID3D11DeviceContext::End</b> in which case the data returned by <b>GetData</b> is accurate up to the last call to <b>ID3D11DeviceContext::End</b>. For information about the queries that only require a call to <b>ID3D11DeviceContext::End</b> and about the type of data that <b>GetData</b> retrieves for each query, see <a href="https://msdn.microsoft.com/4161fbeb-7f58-422c-a195-ea10f737fd0c">D3D11_QUERY</a>.

If <i>DataSize</i> is 0, <b>GetData</b> is only used to check status.

An application gathers counter data by calling <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a>, issuing some graphics commands, calling <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a>, and then calling <b>ID3D11DeviceContext::GetData</b> to get data about what happened in between the <b>Begin</b> and <b>End</b> calls. For information about performance counter types, see <a href="https://msdn.microsoft.com/b6a5cc7e-48e5-478a-aa9c-8b2878c0de6b">D3D11_COUNTER</a>. 




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

