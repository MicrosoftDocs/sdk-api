---
UID: NS:setupapi._SP_INF_INFORMATION
title: "_SP_INF_INFORMATION"
author: windows-sdk-content
description: The SP_INF_INFORMATION structure stores information about an INF file, including the style, number of constituent INF files, and version data.
old-location: setup\sp_inf_information_str.htm
tech.root: SetupApi
ms.assetid: 1fb08456-bc84-41a1-9f02-8fb499801831
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSP_INF_INFORMATION, INF_STYLE_NONE, INF_STYLE_OLDNT, INF_STYLE_WIN4, PSP_INF_INFORMATION, PSP_INF_INFORMATION structure pointer [Setup API], SP_INF_INFORMATION, SP_INF_INFORMATION structure [Setup API], _SP_INF_INFORMATION, _setupapi_sp_inf_information_str, setup.sp_inf_information_str, setupapi/PSP_INF_INFORMATION, setupapi/SP_INF_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: setupapi.h
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
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_INF_INFORMATION
product: Windows
targetos: Windows
req.typenames: SP_INF_INFORMATION, *PSP_INF_INFORMATION
req.redist: 
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



<a href="https://msdn.microsoft.com/837F1864-CE2F-4A9A-A7D9-18EB8622541E">Structures</a>
 

 

