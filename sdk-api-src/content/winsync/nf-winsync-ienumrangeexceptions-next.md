---
UID: NF:winsync.IEnumRangeExceptions.Next
title: IEnumRangeExceptions::Next
author: windows-sdk-content
description: Returns the next elements in the change unit exception set, if they are available.
old-location: winsync\ienumrangeexceptions_next.htm
old-project: winsync
ms.assetid: 0ca472d7-4e97-4998-b883-05329dfdb27a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IEnumRangeExceptions interface [Windows Sync],Next method, IEnumRangeExceptions.Next, IEnumRangeExceptions::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumRangeExceptions interface, winsync.ienumrangeexceptions_next, winsync/IEnumRangeExceptions::Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.redist: 
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
 - IEnumRangeExceptions.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumRangeExceptions::Next


## -description


Returns the next elements in the change unit exception set, if they are available.


## -parameters




### -param cExceptions [in]

The number of range exception elements to retrieve in the range from zero to 1000.


### -param ppRangeException [out]

Returns the next <i>pcFetched</i> range exceptions.


### -param pcFetched [in, out]

Returns the number of range exceptions returned. This value can be <b>NULL</b> only if <i>cExceptions</i> is 1.


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
There are no more elements to retrieve.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1b2724a3-2f5f-4f30-8cf5-e31f16d4cd14">IEnumRangeExceptions Interface</a>
 

 

