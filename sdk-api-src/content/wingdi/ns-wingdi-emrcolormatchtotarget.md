---
UID: NS:wingdi.tagCOLORMATCHTOTARGET
title: EMRCOLORMATCHTOTARGET (wingdi.h)
description: The EMRCOLORMATCHTOTARGET structure contains members for the ColorMatchToTarget enhanced metafile record.
helpviewer_keywords: ["*PEMRCOLORMATCHTOTARGET","EMRCOLORMATCHTOTARGET","EMRCOLORMATCHTOTARGET structure [Windows GDI]","PEMRCOLORMATCHTOTARGET","PEMRCOLORMATCHTOTARGET structure pointer [Windows GDI]","_win32_EMRCOLORMATCHTOTARGET_str","gdi.emrcolormatchtotarget","wingdi/EMRCOLORMATCHTOTARGET","wingdi/PEMRCOLORMATCHTOTARGET"]
old-location: gdi\emrcolormatchtotarget.htm
tech.root: gdi
ms.assetid: 9b89b703-b670-40eb-b95f-d07e8731e71b
ms.date: 12/05/2018
ms.keywords: '*PEMRCOLORMATCHTOTARGET, EMRCOLORMATCHTOTARGET, EMRCOLORMATCHTOTARGET structure [Windows GDI], PEMRCOLORMATCHTOTARGET, PEMRCOLORMATCHTOTARGET structure pointer [Windows GDI], _win32_EMRCOLORMATCHTOTARGET_str, gdi.emrcolormatchtotarget, wingdi/EMRCOLORMATCHTOTARGET, wingdi/PEMRCOLORMATCHTOTARGET'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: EMRCOLORMATCHTOTARGET, *PEMRCOLORMATCHTOTARGET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOLORMATCHTOTARGET
 - wingdi/tagCOLORMATCHTOTARGET
 - PEMRCOLORMATCHTOTARGET
 - wingdi/PEMRCOLORMATCHTOTARGET
 - EMRCOLORMATCHTOTARGET
 - wingdi/EMRCOLORMATCHTOTARGET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRCOLORMATCHTOTARGET
---

# EMRCOLORMATCHTOTARGET structure


## -description

The <b>EMRCOLORMATCHTOTARGET</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-colormatchtotarget">ColorMatchToTarget</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field dwAction

The action to be taken. This member can be one of the following values.

<table>
<tr>
<th>Action</th>
<th>Meaning</th>
</tr>
<tr>
<td>CS_ENABLE</td>
<td>Maps colors to the target device's color gamut. This enables color proofing. All subsequent draw commands to the DC will render colors as they would appear on the target device.</td>
</tr>
<tr>
<td>CS_DISABLE</td>
<td>Disables color proofing.</td>
</tr>
<tr>
<td>CS_DELETE_TRANSFORM</td>
<td>If color management is enabled for the target profile, disables it and deletes the concatenated transform.</td>
</tr>
</table>

### -field dwFlags

This parameter can be the following value.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>COLORMATCHTOTARGET_EMBEDED</td>
<td>Indicates that a color profile has been embedded in the metafile.</td>
</tr>
</table>

### -field cbName

The size of the desired target profile name, in bytes.

### -field cbData

The size of the raw target profile data in bytes, if it is attached.

### -field Data

An array containing the target profile name and the raw target profile data. 
			 The size of the array is <b>cbName</b> + <b>cbData</b>. 
			 If <b>cbData</b> is nonzero the raw target profile data is attached and follows the target profile name at location <b>Data</b>[<b>cbName</b>].

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-colormatchtotarget">ColorMatchToTarget</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>