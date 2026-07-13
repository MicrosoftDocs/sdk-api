---
UID: NF:winsync.ICoreFragment.Reset
title: ICoreFragment::Reset (winsync.h)
description: Resets both the column and range enumerators to the beginning of their respective sets.
helpviewer_keywords: ["ICoreFragment interface [Windows Sync]","Reset method","ICoreFragment.Reset","ICoreFragment::Reset","Reset","Reset method [Windows Sync]","Reset method [Windows Sync]","ICoreFragment interface","winsync.icorefragment_reset","winsync/ICoreFragment::Reset"]
old-location: winsync\icorefragment_reset.htm
tech.root: winsync
ms.assetid: b39e9dee-7437-4480-9050-33bc68b41b00
ms.date: 12/05/2018
ms.keywords: ICoreFragment interface [Windows Sync],Reset method, ICoreFragment.Reset, ICoreFragment::Reset, Reset, Reset method [Windows Sync], Reset method [Windows Sync],ICoreFragment interface, winsync.icorefragment_reset, winsync/ICoreFragment::Reset
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICoreFragment::Reset
 - winsync/ICoreFragment::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ICoreFragment.Reset
---

# ICoreFragment::Reset


## -description

Resets both the column and range enumerators to the beginning of their respective sets.



## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object contained in this object has changed since this object was created.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-icorefragment">ICoreFragment Interface</a>
