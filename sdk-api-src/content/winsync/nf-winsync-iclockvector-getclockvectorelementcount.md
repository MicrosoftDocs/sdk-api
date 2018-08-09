---
UID: NF:winsync.IClockVector.GetClockVectorElementCount
title: IClockVector::GetClockVectorElementCount
author: windows-sdk-content
description: Gets the number of elements that are contained in the clock vector.
old-location: winsync\iclockvector_getclockvectorelementcount.htm
old-project: winsync
ms.assetid: 15ce120e-dabc-4827-b317-82784466c1f1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetClockVectorElementCount, GetClockVectorElementCount method [Windows Sync], GetClockVectorElementCount method [Windows Sync],IClockVector interface, IClockVector interface [Windows Sync],GetClockVectorElementCount method, IClockVector.GetClockVectorElementCount, IClockVector::GetClockVectorElementCount, winsync.iclockvector_getclockvectorelementcount, winsync/IClockVector::GetClockVectorElementCount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IClockVector.GetClockVectorElementCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IClockVector::GetClockVectorElementCount


## -description


Gets the number of elements that are contained in the clock vector.


## -parameters




### -param pdwCount [out]

Returns the number of elements that are contained in the clock vector.


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




<a href="https://msdn.microsoft.com/31aef38d-a6df-4645-a192-9145d3ec90ad">IClockVector Interface</a>
 

 

