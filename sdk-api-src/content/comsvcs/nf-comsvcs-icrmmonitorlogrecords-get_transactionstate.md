---
UID: NF:comsvcs.ICrmMonitorLogRecords.get_TransactionState
title: ICrmMonitorLogRecords::get_TransactionState (comsvcs.h)
description: Retrieves the current state of the transaction.
helpviewer_keywords: ["ICrmMonitorLogRecords interface [COM+]","get_TransactionState method","ICrmMonitorLogRecords.get_TransactionState","ICrmMonitorLogRecords::get_TransactionState","_dtc_ICrmMonitorLogRecords_TransactionState","comsvcs/ICrmMonitorLogRecords::get_TransactionState","cos.icrmmonitorlogrecords_get_transactionstate","get_TransactionState","get_TransactionState method [COM+]","get_TransactionState method [COM+]","ICrmMonitorLogRecords interface"]
old-location: cos\icrmmonitorlogrecords_get_transactionstate.htm
tech.root: cos
ms.assetid: 9aaa3d6c-41b9-4661-8e7e-ef1d1abba4aa
ms.date: 12/05/2018
ms.keywords: ICrmMonitorLogRecords interface [COM+],get_TransactionState method, ICrmMonitorLogRecords.get_TransactionState, ICrmMonitorLogRecords::get_TransactionState, _dtc_ICrmMonitorLogRecords_TransactionState, comsvcs/ICrmMonitorLogRecords::get_TransactionState, cos.icrmmonitorlogrecords_get_transactionstate, get_TransactionState, get_TransactionState method [COM+], get_TransactionState method [COM+],ICrmMonitorLogRecords interface
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
 - ICrmMonitorLogRecords::get_TransactionState
 - comsvcs/ICrmMonitorLogRecords::get_TransactionState
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
 - ICrmMonitorLogRecords.get_TransactionState
---

# ICrmMonitorLogRecords::get_TransactionState


## -description

Retrieves the current state of the transaction.

## -parameters

### -param pVal [out]

The current transaction state, represented by an <a href="/windows/desktop/api/comsvcs/ne-comsvcs-crmtransactionstate">CrmTransactionState</a> enumeration value.

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
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorlogrecords">ICrmMonitorLogRecords</a>