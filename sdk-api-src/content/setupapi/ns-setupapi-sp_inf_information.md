---
UID: NS:setupapi._SP_INF_INFORMATION
title: SP_INF_INFORMATION (setupapi.h)
description: The SP_INF_INFORMATION structure stores information about an INF file, including the style, number of constituent INF files, and version data.
helpviewer_keywords: ["*PSP_INF_INFORMATION","INF_STYLE_NONE","INF_STYLE_OLDNT","INF_STYLE_WIN4","PSP_INF_INFORMATION","PSP_INF_INFORMATION structure pointer [Setup API]","SP_INF_INFORMATION","SP_INF_INFORMATION structure [Setup API]","_setupapi_sp_inf_information_str","setup.sp_inf_information_str","setupapi/PSP_INF_INFORMATION","setupapi/SP_INF_INFORMATION"]
old-location: setup\sp_inf_information_str.htm
tech.root: setup
ms.assetid: 1fb08456-bc84-41a1-9f02-8fb499801831
ms.date: 12/05/2018
ms.keywords: '*PSP_INF_INFORMATION, INF_STYLE_NONE, INF_STYLE_OLDNT, INF_STYLE_WIN4, PSP_INF_INFORMATION, PSP_INF_INFORMATION structure pointer [Setup API], SP_INF_INFORMATION, SP_INF_INFORMATION structure [Setup API], _setupapi_sp_inf_information_str, setup.sp_inf_information_str, setupapi/PSP_INF_INFORMATION, setupapi/SP_INF_INFORMATION'
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
targetos: Windows
req.typenames: SP_INF_INFORMATION, *PSP_INF_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_INF_INFORMATION
 - setupapi/_SP_INF_INFORMATION
 - PSP_INF_INFORMATION
 - setupapi/PSP_INF_INFORMATION
 - SP_INF_INFORMATION
 - setupapi/SP_INF_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_INF_INFORMATION
---

# SP_INF_INFORMATION structure


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

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfinformationa">SetupGetInfInformation</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinffileinformationa">SetupQueryInfFileInformation</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinfversioninformationa">SetupQueryInfVersionInformation</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>