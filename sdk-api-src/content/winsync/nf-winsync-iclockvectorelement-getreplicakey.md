---
UID: NF:winsync.IClockVectorElement.GetReplicaKey
title: IClockVectorElement::GetReplicaKey (winsync.h)
description: Gets the replica key for the replica that is associated with this clock vector element.
helpviewer_keywords: ["GetReplicaKey","GetReplicaKey method [Windows Sync]","GetReplicaKey method [Windows Sync]","IClockVectorElement interface","IClockVectorElement interface [Windows Sync]","GetReplicaKey method","IClockVectorElement.GetReplicaKey","IClockVectorElement::GetReplicaKey","winsync.iclockvectorelement_getreplicakey","winsync/IClockVectorElement::GetReplicaKey"]
old-location: winsync\iclockvectorelement_getreplicakey.htm
tech.root: winsync
ms.assetid: d6f1ce72-e8fd-4f87-a184-7126e880804d
ms.date: 12/05/2018
ms.keywords: GetReplicaKey, GetReplicaKey method [Windows Sync], GetReplicaKey method [Windows Sync],IClockVectorElement interface, IClockVectorElement interface [Windows Sync],GetReplicaKey method, IClockVectorElement.GetReplicaKey, IClockVectorElement::GetReplicaKey, winsync.iclockvectorelement_getreplicakey, winsync/IClockVectorElement::GetReplicaKey
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
 - IClockVectorElement::GetReplicaKey
 - winsync/IClockVectorElement::GetReplicaKey
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
 - IClockVectorElement.GetReplicaKey
---

# IClockVectorElement::GetReplicaKey


## -description

Gets the replica key for the replica that is associated with this clock vector element.

## -parameters

### -param pdwReplicaKey [out]

Returns the replica key for the replica that is associated with this clock vector element.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iclockvectorelement">IClockVectorElement Interface</a>