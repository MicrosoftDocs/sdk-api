---
UID: NF:winsync.ISyncKnowledge.GetScopeVector
title: ISyncKnowledge::GetScopeVector (winsync.h)
description: Gets the clock vector that defines the changes that are contained in the knowledge.
helpviewer_keywords: ["GetScopeVector","GetScopeVector method [Windows Sync]","GetScopeVector method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","GetScopeVector method","ISyncKnowledge.GetScopeVector","ISyncKnowledge::GetScopeVector","winsync.isyncknowledge_getscopevector","winsync/ISyncKnowledge::GetScopeVector"]
old-location: winsync\isyncknowledge_getscopevector.htm
tech.root: winsync
ms.assetid: 92829da0-d9a3-4a91-a60f-6319163e899a
ms.date: 12/05/2018
ms.keywords: GetScopeVector, GetScopeVector method [Windows Sync], GetScopeVector method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetScopeVector method, ISyncKnowledge.GetScopeVector, ISyncKnowledge::GetScopeVector, winsync.isyncknowledge_getscopevector, winsync/ISyncKnowledge::GetScopeVector
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
 - ISyncKnowledge::GetScopeVector
 - winsync/ISyncKnowledge::GetScopeVector
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
 - ISyncKnowledge.GetScopeVector
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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>