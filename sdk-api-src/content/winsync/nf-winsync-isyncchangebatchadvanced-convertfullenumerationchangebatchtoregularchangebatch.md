---
UID: NF:winsync.ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch
title: ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch (winsync.h)
description: Converts an ISyncFullEnumerationChangeBatch object to an ISyncChangeBatch object.
helpviewer_keywords: ["ConvertFullEnumerationChangeBatchToRegularChangeBatch","ConvertFullEnumerationChangeBatchToRegularChangeBatch method [Windows Sync]","ConvertFullEnumerationChangeBatchToRegularChangeBatch method [Windows Sync]","ISyncChangeBatchAdvanced interface","ISyncChangeBatchAdvanced interface [Windows Sync]","ConvertFullEnumerationChangeBatchToRegularChangeBatch method","ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch","ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch","winsync.isyncchangebatchadvanced_convertfullenumerationchangebatchtoregularchangebatch","winsync/ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch"]
old-location: winsync\isyncchangebatchadvanced_convertfullenumerationchangebatchtoregularchangebatch.htm
tech.root: winsync
ms.assetid: 073369ab-232e-410f-b6f1-c43bf15cc652
ms.date: 12/05/2018
ms.keywords: ConvertFullEnumerationChangeBatchToRegularChangeBatch, ConvertFullEnumerationChangeBatchToRegularChangeBatch method [Windows Sync], ConvertFullEnumerationChangeBatchToRegularChangeBatch method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],ConvertFullEnumerationChangeBatchToRegularChangeBatch method, ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch, ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch, winsync.isyncchangebatchadvanced_convertfullenumerationchangebatchtoregularchangebatch, winsync/ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch
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
 - ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch
 - winsync/ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch
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
 - ISyncChangeBatchAdvanced.ConvertFullEnumerationChangeBatchToRegularChangeBatch
---

# ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch


## -description

Converts an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> object to an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> object.

## -parameters

### -param ppChangeBatch [out]

Returns this change batch object, which is represented as an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> object.

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
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
This change batch object is not an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> object.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>