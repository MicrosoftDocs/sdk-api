---
UID: NF:winsync.ISyncKnowledge.GetScopeVector
title: ISyncKnowledge::GetScopeVector
author: windows-sdk-content
description: Gets the clock vector that defines the changes that are contained in the knowledge.
old-location: winsync\isyncknowledge_getscopevector.htm
tech.root: winsync
ms.assetid: 92829da0-d9a3-4a91-a60f-6319163e899a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetScopeVector, GetScopeVector method [Windows Sync], GetScopeVector method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetScopeVector method, ISyncKnowledge.GetScopeVector, ISyncKnowledge::GetScopeVector, winsync.isyncknowledge_getscopevector, winsync/ISyncKnowledge::GetScopeVector
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
 - ISyncKnowledge.GetScopeVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncKnowledge::GetScopeVector


## -description


Gets the clock vector that defines the changes that are contained in the knowledge.


## -parameters




### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IClockVector</b>.


### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that represents the clock vector that defines the changes that are contained in the knowledge.


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
 




## -remarks



Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from <b>GetScopeVector</b>.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 

