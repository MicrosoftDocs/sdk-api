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

# _MODLOAD_DATA structure


## -description


Contains module data.


## -struct-fields




### -field ssize

The size of this structure, in bytes.


### -field ssig

The type of data. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DBHHEADER_DEBUGDIRS"></a><a id="dbhheader_debugdirs"></a><dl>
<dt><b>DBHHEADER_DEBUGDIRS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The <b>data</b> member is a buffer that contains an array of 
<a href="https://msdn.microsoft.com/f89a3c9b-4d73-4ff5-8f45-2e58500d5084">IMAGE_DEBUG_DIRECTORY</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="DBHHEADER_CVMISC"></a><a id="dbhheader_cvmisc"></a><dl>
<dt><b>DBHHEADER_CVMISC</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The <b>data</b> member is a buffer that contains an array of <a href="https://msdn.microsoft.com/24f1ed20-ef7a-4c7b-9bbe-4aaf26c219e7">MODLOAD_CVMISC</a> structures.

</td>
</tr>
</table>
 


### -field data

The data. The format of this data depends on the value of the <b>ssig</b> member.


### -field size

The size of the <b>data</b> buffer, in bytes.


### -field flags

This member is unused.


## -see-also




<a href="https://msdn.microsoft.com/f89a3c9b-4d73-4ff5-8f45-2e58500d5084">IMAGE_DEBUG_DIRECTORY</a>



<a href="https://msdn.microsoft.com/24f1ed20-ef7a-4c7b-9bbe-4aaf26c219e7">MODLOAD_CVMISC</a>



<a href="https://msdn.microsoft.com/4a880090-f063-4d03-8fd5-a57ccba262c8">SymLoadModuleEx</a>
 

 

