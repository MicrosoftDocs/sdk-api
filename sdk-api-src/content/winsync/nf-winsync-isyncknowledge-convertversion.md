---
UID: NF:winsync.ISyncKnowledge.ConvertVersion
title: ISyncKnowledge::ConvertVersion (winsync.h)
description: Converts a version from another replica into one that is compatible with the replica that owns this knowledge.
helpviewer_keywords: ["ConvertVersion","ConvertVersion method [Windows Sync]","ConvertVersion method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","ConvertVersion method","ISyncKnowledge.ConvertVersion","ISyncKnowledge::ConvertVersion","winsync.isyncknowledge_convertversion","winsync/ISyncKnowledge::ConvertVersion"]
old-location: winsync\isyncknowledge_convertversion.htm
tech.root: winsync
ms.assetid: f41edaa3-7c4e-4b2c-9897-474b3e7bfb67
ms.date: 12/05/2018
ms.keywords: ConvertVersion, ConvertVersion method [Windows Sync], ConvertVersion method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],ConvertVersion method, ISyncKnowledge.ConvertVersion, ISyncKnowledge::ConvertVersion, winsync.isyncknowledge_convertversion, winsync/ISyncKnowledge::ConvertVersion
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
 - ISyncKnowledge::ConvertVersion
 - winsync/ISyncKnowledge::ConvertVersion
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
 - ISyncKnowledge.ConvertVersion
---

# ISyncKnowledge::ConvertVersion


## -description

Converts a version from another replica into one that is compatible with the replica that owns this knowledge.

## -parameters

### -param pKnowledgeIn [in]

A knowledge that is valid for <i>pbCurrentOwnerId</i> and that contains <i>pVersionIn</i>.

### -param pbCurrentOwnerId [in]

The ID of the replica that owns <i>pVersionIn</i>.

### -param pVersionIn [in]

The version to convert.

### -param pbNewOwnerId [in]

Returns the ID of the replica that owns the converted version.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbNewOwnerId</i>. Returns the number of bytes required to retrieve the ID when <i>pbNewOwnerId</i> is too small, or returns the number of bytes written.

### -param pVersionOut [out]

Returns the version. This is converted to be valid for the replica that owns this knowledge.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbNewOwnerId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_version">SYNC_VERSION Structure</a>