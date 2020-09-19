---
UID: NF:fci.FNFCISTATUS
title: FNFCISTATUS macro (fci.h)
description: The FNFCISTATUS macro provides the declaration for the application-defined callback function to update the user.
helpviewer_keywords: ["FNFCISTATUS","FNFCISTATUS macro [Windows API]","fci/FNFCISTATUS","winprog.fnfcistatus"]
old-location: winprog\fnfcistatus.htm
tech.root: winprog
ms.assetid: 529fd3c8-9783-4dbe-9268-a9137935cf9b
ms.date: 12/05/2018
ms.keywords: FNFCISTATUS, FNFCISTATUS macro [Windows API], fci/FNFCISTATUS, winprog.fnfcistatus
req.header: fci.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FNFCISTATUS
 - fci/FNFCISTATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCISTATUS
---

## -description

The <b>FNFCISTATUS</b> macro provides the declaration for the application-defined callback function to update the user.

## -parameters

### -param fn

Indicates the type of status update. Possible values include:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>statusFile0x00

</td>
<td>Compressing a block into a folder.</td>
</tr>
<tr>
<td>statusFolder0x01

</td>
<td>Adding a folder to a cabinet.</td>
</tr>
<tr>
<td>statusCabinet0x02

</td>
<td>Writing out a complete cabinet.</td>
</tr>
</table>
 
## -remarks

If  <i>typeStatus</i> equals <b>statusCabinet</b> the returned value indicates the desired size for the cabinet file.  FCI updates the maximum cabinet size remaining using this returned value. This allows a client to generate multiple cabinets per disk, and have FCI limit the size accordingly.

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>