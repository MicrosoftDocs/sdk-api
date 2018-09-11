---
UID: NF:winsync.IEnumClockVector.Skip
title: IEnumClockVector::Skip
author: windows-sdk-content
description: Skips the specified number of clock vector elements.
old-location: winsync\ienumclockvector_skip.htm
tech.root: winsync
ms.assetid: 76f76535-7f1f-431b-9b35-7bbb0d645dcd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumClockVector interface [Windows Sync],Skip method, IEnumClockVector.Skip, IEnumClockVector::Skip, Skip, Skip method [Windows Sync], Skip method [Windows Sync],IEnumClockVector interface, winsync.ienumclockvector_skip, winsync/IEnumClockVector::Skip
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IEnumClockVector.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumClockVector::Skip


## -description


Skips the specified number of clock vector elements.


## -parameters




### -param cSyncVersions [in]

The number of elements to skip.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The enumerator reaches the end of its list before it skips <i>cSyncVersions</i>. In this case, the enumerator skips as many elements as possible.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf191502-dc51-44a7-a82f-a0e38537574f">IEnumClockVector Interface</a>
 

 

