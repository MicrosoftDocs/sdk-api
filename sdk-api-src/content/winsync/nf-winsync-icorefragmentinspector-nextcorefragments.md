---
UID: NF:winsync.ICoreFragmentInspector.NextCoreFragments
title: ICoreFragmentInspector::NextCoreFragments (winsync.h)
description: Returns the next ICoreFragment objects in the knowledge, if they are available.
helpviewer_keywords: ["ICoreFragmentInspector interface [Windows Sync]","NextCoreFragments method","ICoreFragmentInspector.NextCoreFragments","ICoreFragmentInspector::NextCoreFragments","NextCoreFragments","NextCoreFragments method [Windows Sync]","NextCoreFragments method [Windows Sync]","ICoreFragmentInspector interface","winsync.icorefragmentinspector_nextcorefragments","winsync/ICoreFragmentInspector::NextCoreFragments"]
old-location: winsync\icorefragmentinspector_nextcorefragments.htm
tech.root: winsync
ms.assetid: 801a2643-d954-44b8-83ce-021be893d06a
ms.date: 12/05/2018
ms.keywords: ICoreFragmentInspector interface [Windows Sync],NextCoreFragments method, ICoreFragmentInspector.NextCoreFragments, ICoreFragmentInspector::NextCoreFragments, NextCoreFragments, NextCoreFragments method [Windows Sync], NextCoreFragments method [Windows Sync],ICoreFragmentInspector interface, winsync.icorefragmentinspector_nextcorefragments, winsync/ICoreFragmentInspector::NextCoreFragments
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
 - ICoreFragmentInspector::NextCoreFragments
 - winsync/ICoreFragmentInspector::NextCoreFragments
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
 - ICoreFragmentInspector.NextCoreFragments
---

# ICoreFragmentInspector::NextCoreFragments


## -description

Returns the next <b>ICoreFragment</b> objects in the knowledge, if they are available.

## -parameters

### -param requestedCount [in]

The number of <b>ICoreFragment</b> objects to retrieve.

### -param ppiCoreFragments [out]

Receives a pointer to the next <i>pFetchedCount</i> <b>ICoreFragment</b> objects. The size of the array is the value specified in the <i>requestedCount</i> parameter. The length is <code>*(pFetchedCount)</code>. The caller must release the interface pointer.

### -param pFetchedCount [in, out]

Receives the number of <b>ICoreFragment</b> objects that were retrieved in the <i>ppiCoreFragments</i> parameter. This value can be <b>NULL</b> only if <i> requestedCount</i> is 1.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more <b>ICoreFragment</b> objects to retrieve, or the number of <b>ICoreFragment</b> objects retrieved is less than <i>requestedCount</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The knowledge object contained in this object has changed since this object was created.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-icorefragmentinspector">ICoreFragmentInspector Interface</a>