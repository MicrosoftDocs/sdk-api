---
UID: NF:sbe.ISBE2FileScan.RepairFile
title: ISBE2FileScan::RepairFile (sbe.h)
description: Repairs a corrupted .WTV file.
helpviewer_keywords: ["ISBE2FileScan interface [Microsoft TV Technologies]","RepairFile method","ISBE2FileScan.RepairFile","ISBE2FileScan::RepairFile","RepairFile","RepairFile method [Microsoft TV Technologies]","RepairFile method [Microsoft TV Technologies]","ISBE2FileScan interface","mstv.isbe2filescan_repairfile","sbe/ISBE2FileScan::RepairFile"]
old-location: mstv\isbe2filescan_repairfile.htm
tech.root: mstv
ms.assetid: 318eb0e5-2492-4ed4-8a14-764c12024f97
ms.date: 12/05/2018
ms.keywords: ISBE2FileScan interface [Microsoft TV Technologies],RepairFile method, ISBE2FileScan.RepairFile, ISBE2FileScan::RepairFile, RepairFile, RepairFile method [Microsoft TV Technologies], RepairFile method [Microsoft TV Technologies],ISBE2FileScan interface, mstv.isbe2filescan_repairfile, sbe/ISBE2FileScan::RepairFile
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Sbe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISBE2FileScan::RepairFile
 - sbe/ISBE2FileScan::RepairFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2FileScan.RepairFile
---

# ISBE2FileScan::RepairFile


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Repairs a corrupted .WTV file.

You can use this method if you discover possible corruption in a .WTV file and want to restore the last-known good version of the file. The following situations might result in a corrupted file:
<ul>
<li>A process that was creating the file crashed.</li>
<li>Another process was writing to the file (for example, to update metadata) at the same time that the Stream Buffer Engine (SBE) attempted to repair it. SBE tries to fix corrupted .WTV files automatically every time it loads a .WTV file for playback and discovers errors in the file.</li>
</ul>

## -parameters

### -param filename [in]

A pointer to a null-terminated wide-character string that specifies the full path name of the .WTV file.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>INVALID_HANDLE_VALUE</dt>
</dl>
</td>
<td width="60%">
Invalid .WTV file.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2filescan">ISBE2FileScan</a>