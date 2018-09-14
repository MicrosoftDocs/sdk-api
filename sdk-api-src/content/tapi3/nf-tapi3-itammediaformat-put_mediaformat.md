---
UID: NF:tapi3.ITAMMediaFormat.put_MediaFormat
title: ITAMMediaFormat::put_MediaFormat
author: windows-sdk-content
description: The put_MediaFormat method sets the media format.
old-location: tapi3\itammediaformat_put_mediaformat.htm
tech.root: TAPI
ms.assetid: 692df069-3016-46a2-9f33-4c709e85be1b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITAMMediaFormat interface [TAPI 2.2],put_MediaFormat method, ITAMMediaFormat.put_MediaFormat, ITAMMediaFormat::put_MediaFormat, _tapi3_itammediaformat_put_mediaformat, put_MediaFormat, put_MediaFormat method [TAPI 2.2], put_MediaFormat method [TAPI 2.2],ITAMMediaFormat interface, tapi3.itammediaformat_put_mediaformat, tapi3ds/ITAMMediaFormat::put_MediaFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAMMediaFormat.put_MediaFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAMMediaFormat::put_MediaFormat


## -description


The 
<b>put_MediaFormat</b> method sets the media format.


## -parameters




### -param pmt [in]

Pointer to 
<b>AM_MEDIA_TYPE</b> structure. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. 


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



On addresses where a variety of formats are supported (such as Wave MSP addresses, which are used on most modems and voice boards), this call is mandatory or the terminal will not be able to connect.

For other addresses, such as those implemented over IP, the format may be fixed/predetermined. In that case, this call will fail if the format is not the same as the predetermined format. To retrieve such a predetermined format, an application can use 
<a href="https://msdn.microsoft.com/384cd41e-b59a-4ac4-9687-cf0f0738dfe0">get_MediaFormat</a>.




## -see-also




<a href="https://msdn.microsoft.com/82728afe-5743-4b45-86e6-32df021a2a5f">ITAMMediaFormat</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/384cd41e-b59a-4ac4-9687-cf0f0738dfe0">get_MediaFormat</a>
 

 

