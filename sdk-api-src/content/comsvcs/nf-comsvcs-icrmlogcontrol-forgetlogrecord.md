---
UID: NF:comsvcs.ICrmLogControl.ForgetLogRecord
title: ICrmLogControl::ForgetLogRecord (comsvcs.h)
description: Forgets the last log record written by this instance of the interface.
helpviewer_keywords: ["ForgetLogRecord","ForgetLogRecord method [COM+]","ForgetLogRecord method [COM+]","ICrmLogControl interface","ICrmLogControl interface [COM+]","ForgetLogRecord method","ICrmLogControl.ForgetLogRecord","ICrmLogControl::ForgetLogRecord","_dtc_ICrmLogControl_ForgetLogRecord","comsvcs/ICrmLogControl::ForgetLogRecord","cos.icrmlogcontrol_forgetlogrecord"]
old-location: cos\icrmlogcontrol_forgetlogrecord.htm
tech.root: cos
ms.assetid: c1871ca0-0586-41de-9684-2babaafe8796
ms.date: 12/05/2018
ms.keywords: ForgetLogRecord, ForgetLogRecord method [COM+], ForgetLogRecord method [COM+],ICrmLogControl interface, ICrmLogControl interface [COM+],ForgetLogRecord method, ICrmLogControl.ForgetLogRecord, ICrmLogControl::ForgetLogRecord, _dtc_ICrmLogControl_ForgetLogRecord, comsvcs/ICrmLogControl::ForgetLogRecord, cos.icrmlogcontrol_forgetlogrecord
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
 - ICrmLogControl::ForgetLogRecord
 - comsvcs/ICrmLogControl::ForgetLogRecord
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
 - ICrmLogControl.ForgetLogRecord
---

# ICrmLogControl::ForgetLogRecord


## -description

Forgets the last log record written by this instance of the interface.



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no valid log record to forget.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_WRONGSTATE</b></dt>
</dl>
</td>
<td width="60%">
This method was called in the wrong state; either before <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">RegisterCompensator</a> or when the transaction is completing (CRM Worker).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The transaction has aborted, most likely because of a transaction time-out.

</td>
</tr>
</table>

## -remarks

This method can be used to forget only the last record because there is no concept of nesting; that is, write, forget, write, forget is valid, but write, write, forget, forget is not. A log record that has been forgotten is not delivered to the CRM Compensator during transaction outcome notifications.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a>
