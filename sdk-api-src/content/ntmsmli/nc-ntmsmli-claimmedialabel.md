---
UID: NC:ntmsmli.CLAIMMEDIALABEL
title: CLAIMMEDIALABEL (ntmsmli.h)
description: The ClaimMediaLabel callback function determines whether a specified media label was created by the media's associated application.
helpviewer_keywords: ["ClaimMediaLabel","ClaimMediaLabel callback","ClaimMediaLabel callback function [Files]","_zaw_claimmedialabel","base.claimmedialabel","fs.claimmedialabel","ntmsmli/ClaimMediaLabel"]
old-location: fs\claimmedialabel.htm
tech.root: fs
ms.assetid: ac957769-0513-436b-94f0-e3894f7a703b
ms.date: 12/05/2018
ms.keywords: ClaimMediaLabel, ClaimMediaLabel callback, ClaimMediaLabel callback function [Files], _zaw_claimmedialabel, base.claimmedialabel, fs.claimmedialabel, ntmsmli/ClaimMediaLabel
req.header: ntmsmli.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLAIMMEDIALABEL
 - ntmsmli/CLAIMMEDIALABEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - NtmsMli.h
api_name:
 - ClaimMediaLabel
---

# CLAIMMEDIALABEL callback function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<i>ClaimMediaLabel</i> callback function determines whether a specified media label was created by the media's associated application.

## -parameters

### -param pBuffer [in]

Pointer to a buffer that contains the media label.

### -param nBufferSize [in]

Size of the buffer, in bytes.

### -param pLabelInfo [out]

Pointer to a 
<a href="/windows/desktop/api/ntmsmli/ns-ntmsmli-medialabelinfo">MediaLabelInfo</a> structure. The media label library fills in this structure if the library recognizes the media label.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The media label library filled in the 
<a href="/windows/desktop/api/ntmsmli/ns-ntmsmli-medialabelinfo">MediaLabelInfo</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The media label library does not recognize the media label.

</td>
</tr>
</table>

## -remarks

When a media label library uses the 
<i>ClaimMediaLabel</i> function to identify the media label as one created by its associated application, the media label library must fill in the 
<a href="/windows/desktop/api/ntmsmli/ns-ntmsmli-medialabelinfo">MediaLabelInfo</a> structure and return NO_ERROR. If the media label library does not recognize the media label, it returns ERROR_BAD_FORMAT.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Label Library Functions</a>



<a href="/windows/desktop/api/ntmsmli/ns-ntmsmli-medialabelinfo">MediaLabelInfo</a>