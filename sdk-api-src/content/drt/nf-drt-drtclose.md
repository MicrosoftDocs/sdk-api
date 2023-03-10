---
UID: NF:drt.DrtClose
title: DrtClose function (drt.h)
description: DrtClose function closes the local instance of the DRT.
helpviewer_keywords: ["DrtClose","DrtClose function [Peer Networking]","drt/DrtClose","p2p.drtclose"]
old-location: p2p\drtclose.htm
tech.root: p2p
ms.assetid: 37c0a579-64be-4ed6-b1b3-852013875361
ms.date: 12/05/2018
ms.keywords: DrtClose, DrtClose function [Peer Networking], drt/DrtClose, p2p.drtclose
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtClose
 - drt/DrtClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtClose
---

# DrtClose function


## -description

The <b>DrtClose</b> function closes the local instance of the DRT.

## -parameters

### -param hDrt [in]

Handle to the DRT instance.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hDrt</i> handle is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>