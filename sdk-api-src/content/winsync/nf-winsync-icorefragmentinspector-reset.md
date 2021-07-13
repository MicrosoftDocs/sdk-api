---
UID: NF:winsync.ICoreFragmentInspector.Reset
title: ICoreFragmentInspector::Reset (winsync.h)
description: Resets the enumerator to the beginning of the knowledge.
helpviewer_keywords: ["ICoreFragmentInspector interface [Windows Sync]","Reset method","ICoreFragmentInspector.Reset","ICoreFragmentInspector::Reset","Reset","Reset method [Windows Sync]","Reset method [Windows Sync]","ICoreFragmentInspector interface","winsync.icorefragmentinspector_reset","winsync/ICoreFragmentInspector::Reset"]
old-location: winsync\icorefragmentinspector_reset.htm
tech.root: winsync
ms.assetid: 57621ce0-c484-4687-9f2f-98d285b041ca
ms.date: 12/05/2018
ms.keywords: ICoreFragmentInspector interface [Windows Sync],Reset method, ICoreFragmentInspector.Reset, ICoreFragmentInspector::Reset, Reset, Reset method [Windows Sync], Reset method [Windows Sync],ICoreFragmentInspector interface, winsync.icorefragmentinspector_reset, winsync/ICoreFragmentInspector::Reset
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
 - ICoreFragmentInspector::Reset
 - winsync/ICoreFragmentInspector::Reset
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
 - ICoreFragmentInspector.Reset
---

# ICoreFragmentInspector::Reset


## -description

Resets the enumerator to the beginning of the knowledge.



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
The knowledge object that is associated with this object has changed since this object was created.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-icorefragmentinspector">ICoreFragmentInspector Interface</a>
