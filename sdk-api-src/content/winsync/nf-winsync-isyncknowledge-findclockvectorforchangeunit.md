---
UID: NF:winsync.ISyncKnowledge.FindClockVectorForChangeUnit
title: ISyncKnowledge::FindClockVectorForChangeUnit (winsync.h)
description: Gets the clock vector that is associated with the specified change unit ID.
helpviewer_keywords: ["FindClockVectorForChangeUnit","FindClockVectorForChangeUnit method [Windows Sync]","FindClockVectorForChangeUnit method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","FindClockVectorForChangeUnit method","ISyncKnowledge.FindClockVectorForChangeUnit","ISyncKnowledge::FindClockVectorForChangeUnit","winsync.isyncknowledge_findclockvectorforchangeunit","winsync/ISyncKnowledge::FindClockVectorForChangeUnit"]
old-location: winsync\isyncknowledge_findclockvectorforchangeunit.htm
tech.root: winsync
ms.assetid: b5114f66-419f-4fea-87ad-3c2cc43eb2fd
ms.date: 12/05/2018
ms.keywords: FindClockVectorForChangeUnit, FindClockVectorForChangeUnit method [Windows Sync], FindClockVectorForChangeUnit method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],FindClockVectorForChangeUnit method, ISyncKnowledge.FindClockVectorForChangeUnit, ISyncKnowledge::FindClockVectorForChangeUnit, winsync.isyncknowledge_findclockvectorforchangeunit, winsync/ISyncKnowledge::FindClockVectorForChangeUnit
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
 - ISyncKnowledge::FindClockVectorForChangeUnit
 - winsync/ISyncKnowledge::FindClockVectorForChangeUnit
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
 - ISyncKnowledge.FindClockVectorForChangeUnit
---

# ISyncKnowledge::FindClockVectorForChangeUnit


## -description

Gets the clock vector that is associated with the specified change unit ID.

## -parameters

### -param pbItemId [in]

The ID of the item that contains the change unit that is associated with the clock vector to retrieve.

### -param pbChangeUnitId [in]

The ID of the change unit that is associated with the clock vector to retrieve.

### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumClockVector</b>.

### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that can enumerate the list of <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iclockvector">IClockVector</a> objects that is associated with  <i>pbChangeUnitId</i>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>