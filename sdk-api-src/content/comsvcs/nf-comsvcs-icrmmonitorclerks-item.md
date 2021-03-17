---
UID: NF:comsvcs.ICrmMonitorClerks.Item
title: ICrmMonitorClerks::Item (comsvcs.h)
description: Retrieves the instance CLSID of the CRM clerk for the specified index.
helpviewer_keywords: ["ICrmMonitorClerks interface [COM+]","Item method","ICrmMonitorClerks.Item","ICrmMonitorClerks::Item","Item","Item method [COM+]","Item method [COM+]","ICrmMonitorClerks interface","_dtc_ICrmMonitorClerks_Item","comsvcs/ICrmMonitorClerks::Item","cos.icrmmonitorclerks_item"]
old-location: cos\icrmmonitorclerks_item.htm
tech.root: cos
ms.assetid: af25d159-95e6-4695-9350-9a3c1bc034e9
ms.date: 12/05/2018
ms.keywords: ICrmMonitorClerks interface [COM+],Item method, ICrmMonitorClerks.Item, ICrmMonitorClerks::Item, Item, Item method [COM+], Item method [COM+],ICrmMonitorClerks interface, _dtc_ICrmMonitorClerks_Item, comsvcs/ICrmMonitorClerks::Item, cos.icrmmonitorclerks_item
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICrmMonitorClerks::Item
 - comsvcs/ICrmMonitorClerks::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorClerks.Item
---

# ICrmMonitorClerks::Item


## -description

Retrieves the instance CLSID of the CRM clerk for the specified index.

## -parameters

### -param Index [in]

The index of the required CRM clerk as a numeric <b>Variant</b>.

### -param pItem [out]

A pointer to <b>Variant</b> string returning the instance CLSID corresponding to this numeric index.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorclerks">ICrmMonitorClerks</a>