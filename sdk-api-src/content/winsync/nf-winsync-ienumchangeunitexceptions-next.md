---
UID: NF:winsync.IEnumChangeUnitExceptions.Next
title: IEnumChangeUnitExceptions::Next
author: windows-driver-content
description: Returns the next elements in the change unit exception set, if they are available.
old-location: winsync\ienumchangeunitexceptions_next.htm
old-project: winsync
ms.assetid: 97bf473d-4e63-4192-a5d8-b802d5887a55
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IEnumChangeUnitExceptions interface [Windows Sync],Next method, IEnumChangeUnitExceptions.Next, IEnumChangeUnitExceptions::Next, Next, Next method [Windows Sync], Next method [Windows Sync],IEnumChangeUnitExceptions interface, winsync.ienumchangeunitexceptions_next, winsync/IEnumChangeUnitExceptions::Next
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
-	IEnumChangeUnitExceptions.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IEnumChangeUnitExceptions::Next


## -description


Returns the next elements in the change unit exception set, if they are available.


## -parameters




### -param cExceptions [in]

The number of change unit exceptions to retrieve in the range of zero to 1000.


### -param ppChangeUnitException [out]

Returns the next <i>pcFetched</i> change unit exceptions.


### -param pcFetched [in, out]

Returns the number of change unit exceptions that are retrieved. This value can be <b>NULL</b> only if <i>cExceptions</i> is 1.


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
If there are no more change unit exceptions to retrieve.

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




<a href="https://msdn.microsoft.com/40b2977e-f3ae-4ad2-89ed-aacf32b1171e">IEnumChangeUnitExceptions Interface</a>
 

 

