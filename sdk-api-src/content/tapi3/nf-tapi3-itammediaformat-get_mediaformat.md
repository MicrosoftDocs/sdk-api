---
UID: NF:tapi3.ITAMMediaFormat.get_MediaFormat
title: ITAMMediaFormat::get_MediaFormat (tapi3.h)
author: windows-sdk-content
description: The get_MediaFormat method gets the media format.
old-location: tapi3\itammediaformat_get_mediaformat.htm
tech.root: Tapi
ms.assetid: 384cd41e-b59a-4ac4-9687-cf0f0738dfe0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAMMediaFormat interface [TAPI 2.2],get_MediaFormat method, ITAMMediaFormat.get_MediaFormat, ITAMMediaFormat::get_MediaFormat, _tapi3_itammediaformat_get_mediaformat, get_MediaFormat, get_MediaFormat method [TAPI 2.2], get_MediaFormat method [TAPI 2.2],ITAMMediaFormat interface, tapi3.itammediaformat_get_mediaformat, tapi3ds/ITAMMediaFormat::get_MediaFormat
ms.topic: method
f1_keywords: 
 - "tapi3/ITAMMediaFormat.get_MediaFormat"
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
 - ITAMMediaFormat.get_MediaFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAMMediaFormat::get_MediaFormat


## -description


The 
<b>get_MediaFormat</b> method gets the media format.


## -parameters




### -param ppmt [out]

Pointer to an array of 
<b>AM_MEDIA_TYPE</b> structures. For more information on <b>AM_MEDIA_TYPE</b>, see the DirectX documentation. 


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itammediaformat">ITAMMediaFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat">put_MediaFormat</a>
 

 

