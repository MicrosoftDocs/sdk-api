---
UID: NF:winsync.ISyncKnowledge.GetRangeExceptions
title: ISyncKnowledge::GetRangeExceptions (winsync.h)
description: Gets an object that can enumerate the IRangeException objects that are stored in the knowledge.
helpviewer_keywords: ["GetRangeExceptions","GetRangeExceptions method [Windows Sync]","GetRangeExceptions method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","GetRangeExceptions method","ISyncKnowledge.GetRangeExceptions","ISyncKnowledge::GetRangeExceptions","winsync.isyncknowledge_getrangeexceptions","winsync/ISyncKnowledge::GetRangeExceptions"]
old-location: winsync\isyncknowledge_getrangeexceptions.htm
tech.root: winsync
ms.assetid: 9dd945bf-a3e4-408a-bdfe-5163a7dbdc3f
ms.date: 12/05/2018
ms.keywords: GetRangeExceptions, GetRangeExceptions method [Windows Sync], GetRangeExceptions method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetRangeExceptions method, ISyncKnowledge.GetRangeExceptions, ISyncKnowledge::GetRangeExceptions, winsync.isyncknowledge_getrangeexceptions, winsync/ISyncKnowledge::GetRangeExceptions
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
 - ISyncKnowledge::GetRangeExceptions
 - winsync/ISyncKnowledge::GetRangeExceptions
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
 - ISyncKnowledge.GetRangeExceptions
---

# ISyncKnowledge::GetRangeExceptions


## -description

Gets an object that can enumerate the <b>IRangeException</b> objects that are stored in the knowledge.

## -parameters

### -param riid [in]

The IID of the object to retrieve. Must be <b>IID_IEnumRangeExceptions</b>.

### -param ppUnk [out]

Returns an object that implements <i>riid</i> and that can enumerate the list of <b>IRangeException</b> objects that is contained in the knowledge.

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

Be aware that there is no single representation of knowledge. Equivalent knowledge might be represented in different forms and return different values from <b>GetRangeExceptions</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-irangeexception">IRangeException Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>