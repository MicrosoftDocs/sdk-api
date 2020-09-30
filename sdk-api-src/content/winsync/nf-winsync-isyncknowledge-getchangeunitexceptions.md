---
UID: NF:winsync.ISyncKnowledge.GetChangeUnitExceptions
title: ISyncKnowledge::GetChangeUnitExceptions (winsync.h)
description: Gets an object that can enumerate the IChangeUnitException objects that are stored in the knowledge.
helpviewer_keywords: ["GetChangeUnitExceptions","GetChangeUnitExceptions method [Windows Sync]","GetChangeUnitExceptions method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","GetChangeUnitExceptions method","ISyncKnowledge.GetChangeUnitExceptions","ISyncKnowledge::GetChangeUnitExceptions","winsync.isyncknowledge_getchangeunitexceptions","winsync/ISyncKnowledge::GetChangeUnitExceptions"]
old-location: winsync\isyncknowledge_getchangeunitexceptions.htm
tech.root: winsync
ms.assetid: f8d12e76-82f3-4291-8c95-757d4838639e
ms.date: 12/05/2018
ms.keywords: GetChangeUnitExceptions, GetChangeUnitExceptions method [Windows Sync], GetChangeUnitExceptions method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetChangeUnitExceptions method, ISyncKnowledge.GetChangeUnitExceptions, ISyncKnowledge::GetChangeUnitExceptions, winsync.isyncknowledge_getchangeunitexceptions, winsync/ISyncKnowledge::GetChangeUnitExceptions
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
 - ISyncKnowledge::GetChangeUnitExceptions
 - winsync/ISyncKnowledge::GetChangeUnitExceptions
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
 - ISyncKnowledge.GetChangeUnitExceptions
---

# ISyncKnowledge::GetChangeUnitExceptions


## -description

Gets an object that can enumerate the <b>IChangeUnitException</b> objects that are stored in the knowledge.

## -parameters

### -param riid [in]

 The IID of the object to retrieve. Must be <b>IID_IEnumChangeUnitExceptions</b>.

### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that can enumerate the list of <b>IChangeUnitException</b> objects that is contained in the knowledge.

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

Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from <b>GetChangeUnitExceptions</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>