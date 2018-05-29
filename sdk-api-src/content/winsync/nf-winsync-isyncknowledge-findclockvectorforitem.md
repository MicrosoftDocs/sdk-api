---
UID: NF:winsync.ISyncKnowledge.FindClockVectorForItem
title: ISyncKnowledge::FindClockVectorForItem
author: windows-sdk-content
description: Gets the clock vector that is associated with the specified item ID.
old-location: winsync\isyncknowledge_findclockvectorforitem.htm
old-project: winsync
ms.assetid: d0df840c-c0ca-4fd8-b4bd-d4558e21b083
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FindClockVectorForItem, FindClockVectorForItem method [Windows Sync], FindClockVectorForItem method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],FindClockVectorForItem method, ISyncKnowledge.FindClockVectorForItem, ISyncKnowledge::FindClockVectorForItem, winsync.isyncknowledge_findclockvectorforitem, winsync/ISyncKnowledge::FindClockVectorForItem
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncKnowledge.FindClockVectorForItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncKnowledge::FindClockVectorForItem


## -description


Gets the clock vector that is associated with the specified item ID.


## -parameters




### -param pbItemId [in]

The ID of the item that is associated with the clock vector to find.


### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IFeedClockVector</b> or <b>IID_IClockVector</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that represents the clock vector associated with <i>pbItemId</i>.


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
 

 

