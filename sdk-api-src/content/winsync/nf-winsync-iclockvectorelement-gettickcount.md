---
UID: NF:winsync.IClockVectorElement.GetTickCount
title: IClockVectorElement::GetTickCount
author: windows-sdk-content
description: Gets the tick count that defines the upper bound on the range of tick counts that are contained in this clock vector element.
old-location: winsync\iclockvectorelement_gettickcount.htm
tech.root: winsync
ms.assetid: 927d769b-c100-4f5f-a243-c5ca53b4d528
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTickCount, GetTickCount method [Windows Sync], GetTickCount method [Windows Sync],IClockVectorElement interface, IClockVectorElement interface [Windows Sync],GetTickCount method, IClockVectorElement.GetTickCount, IClockVectorElement::GetTickCount, winsync.iclockvectorelement_gettickcount, winsync/IClockVectorElement::GetTickCount
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
 - IClockVectorElement.GetTickCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- IClockVectorElement.GetTickCount
: 
---

# IClockVectorElement::GetTickCount


## -description


Gets the tick count that defines the upper bound on the range of tick counts that are contained in this clock vector element.


## -parameters




### -param pullTickCount [out]

Returns the tick count that defines the upper bound on the range of tick counts that are contained in this clock vector element.


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
 

 

