---
UID: NF:winsync.ISyncKnowledge2.GetInspector
title: ISyncKnowledge2::GetInspector (winsync.h)
description: Returns an object that can be used to retrieve the contents of the knowledge object.
helpviewer_keywords: ["GetInspector","GetInspector method [Windows Sync]","GetInspector method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","GetInspector method","ISyncKnowledge2.GetInspector","ISyncKnowledge2::GetInspector","winsync.isyncknowledge2_getinspector","winsync/ISyncKnowledge2::GetInspector"]
old-location: winsync\isyncknowledge2_getinspector.htm
tech.root: winsync
ms.assetid: 088d864f-bb74-4fd8-b8cb-352cb2731edb
ms.date: 12/05/2018
ms.keywords: GetInspector, GetInspector method [Windows Sync], GetInspector method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetInspector method, ISyncKnowledge2.GetInspector, ISyncKnowledge2::GetInspector, winsync.isyncknowledge2_getinspector, winsync/ISyncKnowledge2::GetInspector
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
 - ISyncKnowledge2::GetInspector
 - winsync/ISyncKnowledge2::GetInspector
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
 - ISyncKnowledge2.GetInspector
---

# ISyncKnowledge2::GetInspector


## -description

Returns an object that can be used to retrieve the contents of the knowledge object.

## -parameters

### -param riid [in]

The IID of the requested inspector. Must be <b>IID_ICoreFragmentInspector</b>.

### -param ppiInspector [out]

An object that implements <i>riid</i>, and that can retrieve the contents of the knowledge object.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
<i>riid</i> is not <b>IID_ICoreFragmentInspector</b>.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>