---
UID: NF:wmcodecdsp.IWMCodecPrivateData.GetPrivateData
title: IWMCodecPrivateData::GetPrivateData (wmcodecdsp.h)
author: windows-sdk-content
description: Retrieves the codec data for the video content based on the output type passed using the IWMCodecPrivateData::SetPartialOutputType method.
old-location: mf\iwmcodecprivatedatagetprivatedata.htm
tech.root: medfound
ms.assetid: 20e61bf6-f242-4f8e-84e6-f6158a0947bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPrivateData, GetPrivateData method [Media Foundation], GetPrivateData method [Media Foundation],IWMCodecPrivateData interface, IWMCodecPrivateData interface [Media Foundation],GetPrivateData method, IWMCodecPrivateData.GetPrivateData, IWMCodecPrivateData::GetPrivateData, codecapi.iwmcodecprivatedatagetprivatedata, mf.iwmcodecprivatedatagetprivatedata, wmcodecdsp/IWMCodecPrivateData::GetPrivateData
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - wmcodecdsp.h
api_name:
 - IWMCodecPrivateData.GetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecPrivateData::GetPrivateData


## -description


Retrieves the codec data for the video content based on the output type passed using the <a href="https://msdn.microsoft.com/c906ac2d-b3e0-4ecd-8f0e-3fa1a2a0beea">IWMCodecPrivateData::SetPartialOutputType</a> method.



## -parameters




### -param pbData [out]

Address of the buffer that receives the private data. If you set this to <b>NULL</b>, the size required to hold the private data will be returned in <i>pcbData</i>.


### -param pcbData [in, out]

Pointer to the size of the private data in bytes. If pbData is <b>NULL</b>, the method will set this to the correct value.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If you are setting properties on the encoder object, you must finish that configuration before getting the private data. Changing properties invalidates any private data that was previously retrieved. If you change properties after getting the private data, retrieve it again and reset the output type.

You must call this method after providing the codec with the output media type (without the private data appended) by calling <a href="https://msdn.microsoft.com/c906ac2d-b3e0-4ecd-8f0e-3fa1a2a0beea">IWMCodecPrivateData::SetPartialOutputType</a>.

After retrieving the private data, allocate a buffer the size of VIDEOINFOHEADER plus <i>pcbData</i>. Then copy the data from your partial output type to the beginning of the buffer and append the private data. 




## -see-also




<a href="https://msdn.microsoft.com/c1216fd7-7cbd-45cf-b694-a5fd9a972fcd">IWMCodecPrivateData Interface</a>
 

 

