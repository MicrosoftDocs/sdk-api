---
UID: NF:comsvcs.ICrmMonitor.HoldClerk
title: ICrmMonitor::HoldClerk (comsvcs.h)
description: Retrieves a pointer on the specified clerk.
helpviewer_keywords: ["HoldClerk","HoldClerk method [COM+]","HoldClerk method [COM+]","ICrmMonitor interface","ICrmMonitor interface [COM+]","HoldClerk method","ICrmMonitor.HoldClerk","ICrmMonitor::HoldClerk","_dtc_ICrmMonitor_HoldClerk","comsvcs/ICrmMonitor::HoldClerk","cos.icrmmonitor_holdclerk"]
old-location: cos\icrmmonitor_holdclerk.htm
tech.root: cos
ms.assetid: 8e0f5197-d423-4b74-aaa1-2ec60e01d75c
ms.date: 12/05/2018
ms.keywords: HoldClerk, HoldClerk method [COM+], HoldClerk method [COM+],ICrmMonitor interface, ICrmMonitor interface [COM+],HoldClerk method, ICrmMonitor.HoldClerk, ICrmMonitor::HoldClerk, _dtc_ICrmMonitor_HoldClerk, comsvcs/ICrmMonitor::HoldClerk, cos.icrmmonitor_holdclerk
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
 - ICrmMonitor::HoldClerk
 - comsvcs/ICrmMonitor::HoldClerk
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
 - ICrmMonitor.HoldClerk
---

# ICrmMonitor::HoldClerk


## -description

Retrieves a pointer on the specified clerk.

## -parameters

### -param Index [in]

A <b>VARIANT</b> string containing the instance CLSID of the required CRM clerk.

### -param pItem [out]

A <b>VARIANT</b> <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer returning the interface to the specified CRM clerk.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_CLERKNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified CRM clerk was not found. It may have completed before it could be held.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitor">ICrmMonitor</a>