---
UID: NF:comsvcs.ICrmMonitor.GetClerks
title: ICrmMonitor::GetClerks (comsvcs.h)
description: Retrieves a clerk collection object, which is a snapshot of the current state of the clerks.
helpviewer_keywords: ["GetClerks","GetClerks method [COM+]","GetClerks method [COM+]","ICrmMonitor interface","ICrmMonitor interface [COM+]","GetClerks method","ICrmMonitor.GetClerks","ICrmMonitor::GetClerks","_dtc_ICrmMonitor_GetClerks","comsvcs/ICrmMonitor::GetClerks","cos.icrmmonitor_getclerks"]
old-location: cos\icrmmonitor_getclerks.htm
tech.root: cos
ms.assetid: b5802d3b-1464-4ddf-b459-a308b699de96
ms.date: 12/05/2018
ms.keywords: GetClerks, GetClerks method [COM+], GetClerks method [COM+],ICrmMonitor interface, ICrmMonitor interface [COM+],GetClerks method, ICrmMonitor.GetClerks, ICrmMonitor::GetClerks, _dtc_ICrmMonitor_GetClerks, comsvcs/ICrmMonitor::GetClerks, cos.icrmmonitor_getclerks
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
 - ICrmMonitor::GetClerks
 - comsvcs/ICrmMonitor::GetClerks
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
 - ICrmMonitor.GetClerks
---

# ICrmMonitor::GetClerks


## -description

Retrieves a clerk collection object, which is a snapshot of the current state of the clerks.

## -parameters

### -param pClerks [out]

An <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorclerks">ICrmMonitorClerks</a> pointer to a clerks collection object.

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
<dt><b>XACT_E_RECOVERYINPROGRESS</b></dt>
</dl>
</td>
<td width="60%">
Recovery of the CRM log file is still in progress.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitor">ICrmMonitor</a>