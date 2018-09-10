---
UID: NF:segment.IMSVidStreamBufferSource.put_BlockUnrated
title: IMSVidStreamBufferSource::put_BlockUnrated
author: windows-sdk-content
description: The put_BlockUnrated method specifies whether to block unrated content.
old-location: mstv\imsvidstreambuffersource_put_blockunrated.htm
tech.root: mstv
ms.assetid: 9dd59b87-708b-4003-9575-54a02b97c272
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],put_BlockUnrated method, IMSVidStreamBufferSource.put_BlockUnrated, IMSVidStreamBufferSource::put_BlockUnrated, IMSVidStreamBufferSourceput_BlockUnrated, mstv.imsvidstreambuffersource_put_blockunrated, put_BlockUnrated, put_BlockUnrated method [Microsoft TV Technologies], put_BlockUnrated method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, segment/IMSVidStreamBufferSource::put_BlockUnrated
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidStreamBufferSource.put_BlockUnrated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidStreamBufferSource::put_BlockUnrated


## -description


The <b>put_BlockUnrated</b> method specifies whether to block unrated content.


## -parameters




### -param bBlock [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>Do not block unrated content.</td>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>Block unrated content.</td>
</tr>
</table>
 


## -returns



The method returns an <b>HRESULT</b>. Possible values include the following.

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
 




## -see-also




<a href="https://msdn.microsoft.com/12160959-820b-4534-9392-a13ad229317d">IMSVidStreamBufferSource Interface</a>



<a href="https://msdn.microsoft.com/7b4e1ac4-dfb8-45c0-9079-16f8babcb494">IMSVidStreamBufferSource::put_UnratedDelay</a>
 

 

