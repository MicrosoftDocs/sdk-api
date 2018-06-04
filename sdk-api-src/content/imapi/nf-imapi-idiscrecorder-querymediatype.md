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

# IDiscRecorder::QueryMediaType


## -description


Detects the type of media currently inserted in the recorder, if any.


## -parameters




### -param fMediaType [out]

If there is no media, both <i>fMediaType</i> and <i>fMediaFlags</i> are zero. If there is media, <i>fMediaType</i> contains one or more of the following values. 



					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_EXTRA"></a><a id="media_cd_extra"></a><dl>
<dt><b>MEDIA_CD_EXTRA</b></dt>
</dl>
</td>
<td width="60%">
4

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_I"></a><a id="media_cd_i"></a><dl>
<dt><b>MEDIA_CD_I</b></dt>
</dl>
</td>
<td width="60%">
3

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_OTHER"></a><a id="media_cd_other"></a><dl>
<dt><b>MEDIA_CD_OTHER</b></dt>
</dl>
</td>
<td width="60%">
5

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_ROM_XA"></a><a id="media_cd_rom_xa"></a><dl>
<dt><b>MEDIA_CD_ROM_XA</b></dt>
</dl>
</td>
<td width="60%">
2

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CDDA_CDROM"></a><a id="media_cdda_cdrom"></a><dl>
<dt><b>MEDIA_CDDA_CDROM</b></dt>
</dl>
</td>
<td width="60%">
1

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_SPECIAL"></a><a id="media_special"></a><dl>
<dt><b>MEDIA_SPECIAL</b></dt>
</dl>
</td>
<td width="60%">
6

</td>
</tr>
</table>
 


### -param fMediaFlags [out]

If there is media, this parameter contains one or more of the following values. 



					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEDIA_BLANK"></a><a id="media_blank"></a><dl>
<dt><b>MEDIA_BLANK</b></dt>
</dl>
</td>
<td width="60%">
0x1

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_RW"></a><a id="media_rw"></a><dl>
<dt><b>MEDIA_RW</b></dt>
</dl>
</td>
<td width="60%">
0x2

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_WRITABLE"></a><a id="media_writable"></a><dl>
<dt><b>MEDIA_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
0x4

</td>
</tr>
</table>
 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

