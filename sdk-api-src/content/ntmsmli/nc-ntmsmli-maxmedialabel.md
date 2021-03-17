---
UID: NC:ntmsmli.MAXMEDIALABEL
title: MAXMEDIALABEL (ntmsmli.h)
description: The MaxMediaLabel callback function determines the maximum size of the media label for the applications supported by the media label library.
helpviewer_keywords: ["MaxMediaLabel","MaxMediaLabel callback","MaxMediaLabel callback function [Files]","_zaw_maxmedialabel","base.maxmedialabel","fs.maxmedialabel","ntmsmli/MaxMediaLabel"]
old-location: fs\maxmedialabel.htm
tech.root: fs
ms.assetid: b770cc63-e1dd-4d1a-8009-8e1bdc9ce69c
ms.date: 12/05/2018
ms.keywords: MaxMediaLabel, MaxMediaLabel callback, MaxMediaLabel callback function [Files], _zaw_maxmedialabel, base.maxmedialabel, fs.maxmedialabel, ntmsmli/MaxMediaLabel
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
 - MAXMEDIALABEL
 - ntmsmli/MAXMEDIALABEL
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
 - MaxMediaLabel
---

# MAXMEDIALABEL callback function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<i>MaxMediaLabel</i> callback function determines the maximum size of the media label for the applications supported by the media label library.

## -parameters

### -param pMaxSize [out]

Pointer to a buffer that receives the maximum size of the buffer sent to the 
<a href="/windows/desktop/api/ntmsmli/nc-ntmsmli-claimmedialabel">ClaimMediaLabel</a> function.

## -returns

This function returns the following value.

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
The function was successful.

</td>
</tr>
</table>

## -remarks

When the media format of the media specified in the 
<i>MaxMediaLabel</i> function does not have a theoretical size limit, the application should return the size of the largest media label the application can possibly generate.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Label Library Functions</a>