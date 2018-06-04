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

# IServiceLocationDescriptor::GetElementStreamType


## -description


Gets a code identifying the type of an elementary stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor. 


## -parameters




### -param bIndex [in]

Specifies the elementary stream,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/134e4051-6a73-4420-b12d-3171738bd8ad">IServiceLocationDescriptor::GetNumberOfElements</a>
  method to get the number of elementary streams in the descriptor.


### -param pbVal [out]

Receives the element stream type code. This can be any of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
ITU-T | ISO/IEC Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01-0x7F</dt>
</dl>
</td>
<td width="60%">
As specified in Table 2.29 (Stream type assignments)
of <i>ITU-T Rec. H.222.0 | ISO/IEC 13818-1:1996, Information Technology — Generic
coding of moving pictures and associated audio — Part 1: Systems (normative)</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
[Used in other systems.]

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x81</dt>
</dl>
</td>
<td width="60%">
ATSC A/53 audio.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x82-0x84</dt>
</dl>
</td>
<td width="60%">
[Used in other systems.]

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x85</dt>
</dl>
</td>
<td width="60%">
UPID that is defined in <i>ATSC Standard A/57 (1996), Program/Episode/Version Identification (normative).</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x86-0xBF</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0xC0-0xFF</dt>
</dl>
</td>
<td width="60%">
User Private.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/43dd800b-c51d-4a2f-ad59-943cb4975066">IServiceLocationDescriptor</a>



<a href="https://msdn.microsoft.com/134e4051-6a73-4420-b12d-3171738bd8ad">IServiceLocationDescriptor::GetNumberOfElements</a>
 

 

