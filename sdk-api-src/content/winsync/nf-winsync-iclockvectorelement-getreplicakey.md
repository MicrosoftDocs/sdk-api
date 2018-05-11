---
UID: NF:winsync.IClockVectorElement.GetReplicaKey
title: IClockVectorElement::GetReplicaKey
author: windows-driver-content
description: Gets the replica key for the replica that is associated with this clock vector element.
old-location: winsync\iclockvectorelement_getreplicakey.htm
old-project: winsync
ms.assetid: d6f1ce72-e8fd-4f87-a184-7126e880804d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetReplicaKey, GetReplicaKey method [Windows Sync], GetReplicaKey method [Windows Sync],IClockVectorElement interface, IClockVectorElement interface [Windows Sync],GetReplicaKey method, IClockVectorElement.GetReplicaKey, IClockVectorElement::GetReplicaKey, winsync.iclockvectorelement_getreplicakey, winsync/IClockVectorElement::GetReplicaKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IClockVectorElement.GetReplicaKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/cae24ef0-5b31-48c2-99bd-9e0954ec3b37">IClockVectorElement Interface</a>
 

 

