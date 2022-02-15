---
UID: NF:comsvcs.ICrmLogControl.ForceTransactionToAbort
title: ICrmLogControl::ForceTransactionToAbort (comsvcs.h)
description: Performs an immediate abort call on the transaction.
helpviewer_keywords: ["ForceTransactionToAbort","ForceTransactionToAbort method [COM+]","ForceTransactionToAbort method [COM+]","ICrmLogControl interface","ICrmLogControl interface [COM+]","ForceTransactionToAbort method","ICrmLogControl.ForceTransactionToAbort","ICrmLogControl::ForceTransactionToAbort","_dtc_ICrmLogControl_ForceTransactionToAbort","comsvcs/ICrmLogControl::ForceTransactionToAbort","cos.icrmlogcontrol_forcetransactiontoabort"]
old-location: cos\icrmlogcontrol_forcetransactiontoabort.htm
tech.root: cos
ms.assetid: 5a0289c6-d177-40a3-968d-96ae3179e78d
ms.date: 12/05/2018
ms.keywords: ForceTransactionToAbort, ForceTransactionToAbort method [COM+], ForceTransactionToAbort method [COM+],ICrmLogControl interface, ICrmLogControl interface [COM+],ForceTransactionToAbort method, ICrmLogControl.ForceTransactionToAbort, ICrmLogControl::ForceTransactionToAbort, _dtc_ICrmLogControl_ForceTransactionToAbort, comsvcs/ICrmLogControl::ForceTransactionToAbort, cos.icrmlogcontrol_forcetransactiontoabort
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
 - ICrmLogControl::ForceTransactionToAbort
 - comsvcs/ICrmLogControl::ForceTransactionToAbort
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
 - ICrmLogControl.ForceTransactionToAbort
---

# ICrmLogControl::ForceTransactionToAbort


## -description

Performs an immediate abort call on the transaction.



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

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a>
