---
UID: NF:winsync.ISyncKnowledge2.GetKnowledgeCookie
title: ISyncKnowledge2::GetKnowledgeCookie (winsync.h)
description: Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons.
helpviewer_keywords: ["GetKnowledgeCookie","GetKnowledgeCookie method [Windows Sync]","GetKnowledgeCookie method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","GetKnowledgeCookie method","ISyncKnowledge2.GetKnowledgeCookie","ISyncKnowledge2::GetKnowledgeCookie","winsync.isyncknowledge2_getknowledgecookie","winsync/ISyncKnowledge2::GetKnowledgeCookie"]
old-location: winsync\isyncknowledge2_getknowledgecookie.htm
tech.root: winsync
ms.assetid: d182f81d-131c-4f18-85e4-ff675ae99888
ms.date: 12/05/2018
ms.keywords: GetKnowledgeCookie, GetKnowledgeCookie method [Windows Sync], GetKnowledgeCookie method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetKnowledgeCookie method, ISyncKnowledge2.GetKnowledgeCookie, ISyncKnowledge2::GetKnowledgeCookie, winsync.isyncknowledge2_getknowledgecookie, winsync/ISyncKnowledge2::GetKnowledgeCookie
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
 - ISyncKnowledge2::GetKnowledgeCookie
 - winsync/ISyncKnowledge2::GetKnowledgeCookie
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
 - ISyncKnowledge2.GetKnowledgeCookie
---

# ISyncKnowledge2::GetKnowledgeCookie


## -description

Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons.

## -parameters

### -param ppKnowledgeCookie [out]

A lightweight, read-only representation of this knowledge object that can be used for fast comparisons.

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

## -remarks

A knowledge cookie can be used for fast comparisons with other knowledge objects by using <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-comparetoknowledgecookie">ISyncKnowledge2::CompareToKnowledgeCookie</a> when the performance of the comparison operation is especially important.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>