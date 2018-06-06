---
UID: NF:winsync.ISyncKnowledge.FindClockVectorForChangeUnit
title: ISyncKnowledge::FindClockVectorForChangeUnit
author: windows-sdk-content
description: Gets the clock vector that is associated with the specified change unit ID.
old-location: winsync\isyncknowledge_findclockvectorforchangeunit.htm
old-project: winsync
ms.assetid: b5114f66-419f-4fea-87ad-3c2cc43eb2fd
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FindClockVectorForChangeUnit, FindClockVectorForChangeUnit method [Windows Sync], FindClockVectorForChangeUnit method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],FindClockVectorForChangeUnit method, ISyncKnowledge.FindClockVectorForChangeUnit, ISyncKnowledge::FindClockVectorForChangeUnit, winsync.isyncknowledge_findclockvectorforchangeunit, winsync/ISyncKnowledge::FindClockVectorForChangeUnit
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
 - ISyncKnowledge.FindClockVectorForChangeUnit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

Returns an object that implements <i>riid</i> and that can enumerate the list of <a href="https://msdn.microsoft.com/31aef38d-a6df-4645-a192-9145d3ec90ad">IClockVector</a> objects that is associated with  <i>pbChangeUnitId</i>.


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




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

