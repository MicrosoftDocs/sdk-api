---
UID: NF:winsync.ISyncChangeBatchBase.GetSourceForgottenKnowledge
title: ISyncChangeBatchBase::GetSourceForgottenKnowledge (winsync.h)
description: Gets the forgotten knowledge of the source replica.
helpviewer_keywords: ["GetSourceForgottenKnowledge","GetSourceForgottenKnowledge method [Windows Sync]","GetSourceForgottenKnowledge method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","GetSourceForgottenKnowledge method","ISyncChangeBatchBase.GetSourceForgottenKnowledge","ISyncChangeBatchBase::GetSourceForgottenKnowledge","winsync.isyncchangebatchbase_getsourceforgottenknowledge","winsync/ISyncChangeBatchBase::GetSourceForgottenKnowledge"]
old-location: winsync\isyncchangebatchbase_getsourceforgottenknowledge.htm
tech.root: winsync
ms.assetid: 309b2c83-4480-421c-ae90-9cbe7ac11055
ms.date: 12/05/2018
ms.keywords: GetSourceForgottenKnowledge, GetSourceForgottenKnowledge method [Windows Sync], GetSourceForgottenKnowledge method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetSourceForgottenKnowledge method, ISyncChangeBatchBase.GetSourceForgottenKnowledge, ISyncChangeBatchBase::GetSourceForgottenKnowledge, winsync.isyncchangebatchbase_getsourceforgottenknowledge, winsync/ISyncChangeBatchBase::GetSourceForgottenKnowledge
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
 - ISyncChangeBatchBase::GetSourceForgottenKnowledge
 - winsync/ISyncChangeBatchBase::GetSourceForgottenKnowledge
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
 - ISyncChangeBatchBase.GetSourceForgottenKnowledge
---

# ISyncChangeBatchBase::GetSourceForgottenKnowledge


## -description

Gets the forgotten knowledge of the source replica.

## -parameters

### -param ppSourceForgottenKnowledge [out]

Returns the forgotten knowledge of the source replica.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>