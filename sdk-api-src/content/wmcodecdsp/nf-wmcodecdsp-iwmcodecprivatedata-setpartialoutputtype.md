---
UID: NF:wmcodecdsp.IWMCodecPrivateData.SetPartialOutputType
title: IWMCodecPrivateData::SetPartialOutputType
author: windows-sdk-content
description: Gives the codec the output media type without the codec data. This enables the codec to generate the private data.
old-location: mf\iwmcodecprivatedatasetpartialoutputtype.htm
tech.root: medfound
ms.assetid: c906ac2d-b3e0-4ecd-8f0e-3fa1a2a0beea
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IWMCodecPrivateData interface [Media Foundation],SetPartialOutputType method, IWMCodecPrivateData.SetPartialOutputType, IWMCodecPrivateData::SetPartialOutputType, SetPartialOutputType, SetPartialOutputType method [Media Foundation], SetPartialOutputType method [Media Foundation],IWMCodecPrivateData interface, codecapi.iwmcodecprivatedatasetpartialoutputtype, mf.iwmcodecprivatedatasetpartialoutputtype, wmcodecdsp/IWMCodecPrivateData::SetPartialOutputType
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMCodecPrivateData.SetPartialOutputType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMCodecPrivateData::SetPartialOutputType


## -description


Gives the codec the output media type without the codec data. This enables the codec to generate the private data.



## -parameters




### -param pmt [in]

Address of the partial output media type.


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



The DMO_MEDIA_TYPE that you pass to this method is only partial in that it does not include the appended private data. It must be complete in all other ways.

If you are setting properties on an encoder, you must finish that configuration before getting the private data. Changing properties invalidates any private data previously retrieved. If you change properties after getting the private data, retrieve it again and reset the output type.

You must call this method before calling <a href="https://msdn.microsoft.com/20e61bf6-f242-4f8e-84e6-f6158a0947bc">IWMCodecPrivateData::GetPrivateData</a> to get the private data.




## -see-also




<a href="https://msdn.microsoft.com/c1216fd7-7cbd-45cf-b694-a5fd9a972fcd">IWMCodecPrivateData Interface</a>
 

 

