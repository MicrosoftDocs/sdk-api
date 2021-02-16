---
UID: NF:winsync.ISyncKnowledge.GetVersion
title: ISyncKnowledge::GetVersion (winsync.h)
description: Gets the version of this knowledge structure.
helpviewer_keywords: ["GetVersion","GetVersion method [Windows Sync]","GetVersion method [Windows Sync]","ISyncKnowledge interface","ISyncKnowledge interface [Windows Sync]","GetVersion method","ISyncKnowledge.GetVersion","ISyncKnowledge::GetVersion","winsync.isyncknowledge_getversion","winsync/ISyncKnowledge::GetVersion"]
old-location: winsync\isyncknowledge_getversion.htm
tech.root: winsync
ms.assetid: b54114f1-aa54-493d-b449-0b9161004ffa
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [Windows Sync], GetVersion method [Windows Sync],ISyncKnowledge interface, ISyncKnowledge interface [Windows Sync],GetVersion method, ISyncKnowledge.GetVersion, ISyncKnowledge::GetVersion, winsync.isyncknowledge_getversion, winsync/ISyncKnowledge::GetVersion
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
 - ISyncKnowledge::GetVersion
 - winsync/ISyncKnowledge::GetVersion
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
 - ISyncKnowledge.GetVersion
---

# ISyncKnowledge::GetVersion


## -description

Gets the version of this knowledge structure.

## -parameters

### -param pdwVersion [out]

Returns the version of this knowledge structure. is one of the values in the <a href="/windows/win32/api/winsync/ne-winsync-sync_serialization_version">SYNC_SERIALIZATION_VERSION</a> enumeration.

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

This value is the version of the knowledge structure itself. When the internal knowledge structure is changed, the version that this method returns will also be changed.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_serialization_version">SYNC_SERIALIZATION_VERSION Enumeration</a>