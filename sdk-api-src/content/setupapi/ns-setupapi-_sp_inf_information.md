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

# _SP_INF_INFORMATION structure


## -description


The 
<b>SP_INF_INFORMATION</b> structure stores information about an INF file, including the style, number of constituent INF files, and version data.


## -struct-fields




### -field InfStyle

Style of the INF file. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INF_STYLE_NONE"></a><a id="inf_style_none"></a><dl>
<dt><b>INF_STYLE_NONE</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the style of the INF file is unrecognized or nonexistent.

</td>
</tr>
<tr>
<td width="40%"><a id="INF_STYLE_OLDNT"></a><a id="inf_style_oldnt"></a><dl>
<dt><b>INF_STYLE_OLDNT</b></dt>
</dl>
</td>
<td width="60%">
A legacy INF file format.

</td>
</tr>
<tr>
<td width="40%"><a id="INF_STYLE_WIN4"></a><a id="inf_style_win4"></a><dl>
<dt><b>INF_STYLE_WIN4</b></dt>
</dl>
</td>
<td width="60%">
A Windows INF file format.

</td>
</tr>
</table>
 


### -field InfCount

Number of constituent INF files.


### -field VersionData

Stores information from the <b>Version</b> section of an INF file in an array of <b>ANYSIZE_ARRAY</b> bytes.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/367eb374-1295-41f6-a1b3-cfc04e94b816">SetupGetInfInformation</a>



<a href="https://msdn.microsoft.com/36f1824d-f71e-462a-a233-0240e76de3d2">SetupQueryInfFileInformation</a>



<a href="https://msdn.microsoft.com/58768b91-a0c7-4791-8667-2890b742798c">SetupQueryInfVersionInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

