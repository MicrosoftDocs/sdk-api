---
UID: NF:strmif.IEncoderAPI.IsSupported
title: IEncoderAPI::IsSupported
author: windows-sdk-content
description: The IsSupported method queries whether a given parameter is supported.
old-location: mstv\iencoderapi_issupported.htm
tech.root: mstv
ms.assetid: bbcbde18-2b2d-48b0-9f52-185648f502ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEncoderAPI interface [Microsoft TV Technologies],IsSupported method, IEncoderAPI.IsSupported, IEncoderAPI::IsSupported, IEncoderAPIIsSupported, IsSupported, IsSupported method [Microsoft TV Technologies], IsSupported method [Microsoft TV Technologies],IEncoderAPI interface, mstv.iencoderapi_issupported, strmif/IEncoderAPI::IsSupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEncoderAPI.IsSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEncoderAPI::IsSupported


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI</a> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>IsSupported</b> method queries whether a given parameter is supported.


## -parameters




### -param Api [in]

Pointer to a GUID that specifies the parameter.
          


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
The encoder supports the parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The encoder does not support the parameter.

</td>
</tr>
</table>
 




## -remarks



The method returns S_OK if the encoder recognizes the GUID. To check whether the parameter can be read or modified, call the <a href="https://msdn.microsoft.com/ad94b70f-fd35-44b4-8322-9891cd7f17cc">IEncoderAPI::IsAvailable</a> method.
      

Any errors besides those in the table above indicate an inability to process the call.
      




## -see-also




<a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>



<a href="https://msdn.microsoft.com/823b79a1-1bf5-4aab-80dd-0e77ba950127">IEncoderAPI Interface</a>
 

 

