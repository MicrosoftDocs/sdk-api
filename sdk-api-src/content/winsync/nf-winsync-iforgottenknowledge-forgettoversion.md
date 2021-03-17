---
UID: NF:winsync.IForgottenKnowledge.ForgetToVersion
title: IForgottenKnowledge::ForgetToVersion (winsync.h)
description: Updates the forgotten knowledge to reflect that all versions that are less than or equal to the specified version might have been forgotten, and that corresponding tombstones might have been deleted.
helpviewer_keywords: ["ForgetToVersion","ForgetToVersion method [Windows Sync]","ForgetToVersion method [Windows Sync]","IForgottenKnowledge interface","IForgottenKnowledge interface [Windows Sync]","ForgetToVersion method","IForgottenKnowledge.ForgetToVersion","IForgottenKnowledge::ForgetToVersion","winsync.iforgottenknowledge_forgettoversion","winsync/IForgottenKnowledge::ForgetToVersion"]
old-location: winsync\iforgottenknowledge_forgettoversion.htm
tech.root: winsync
ms.assetid: 63ea1fdc-5200-40d4-a42a-dcda0318f602
ms.date: 12/05/2018
ms.keywords: ForgetToVersion, ForgetToVersion method [Windows Sync], ForgetToVersion method [Windows Sync],IForgottenKnowledge interface, IForgottenKnowledge interface [Windows Sync],ForgetToVersion method, IForgottenKnowledge.ForgetToVersion, IForgottenKnowledge::ForgetToVersion, winsync.iforgottenknowledge_forgettoversion, winsync/IForgottenKnowledge::ForgetToVersion
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
 - IForgottenKnowledge::ForgetToVersion
 - winsync/IForgottenKnowledge::ForgetToVersion
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
 - IForgottenKnowledge.ForgetToVersion
---

# IForgottenKnowledge::ForgetToVersion


## -description

Updates the forgotten knowledge to reflect that all versions that are less than or equal to the specified version might have been forgotten, and that corresponding tombstones might have been deleted.

## -parameters

### -param pKnowledge [in]

The current knowledge of the replica that owns this forgotten knowledge object.

### -param pVersion [in]

The version of the tombstone that has been cleaned up.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

When a replica cleans up the tombstone for an item, its associated provider must call this method and specify the version of the tombstone that was removed.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iforgottenknowledge">IForgottenKnowledge Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC_VERSION Structure</a>