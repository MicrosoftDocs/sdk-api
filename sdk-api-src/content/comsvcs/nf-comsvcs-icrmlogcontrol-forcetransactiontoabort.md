---
UID: NF:comsvcs.ICrmLogControl.ForceTransactionToAbort
title: ICrmLogControl::ForceTransactionToAbort
author: windows-sdk-content
description: Performs an immediate abort call on the transaction.
old-location: cos\icrmlogcontrol_forcetransactiontoabort.htm
tech.root: cossdk
ms.assetid: 5a0289c6-d177-40a3-968d-96ae3179e78d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ForceTransactionToAbort, ForceTransactionToAbort method [COM+], ForceTransactionToAbort method [COM+],ICrmLogControl interface, ICrmLogControl interface [COM+],ForceTransactionToAbort method, ICrmLogControl.ForceTransactionToAbort, ICrmLogControl::ForceTransactionToAbort, _dtc_ICrmLogControl_ForceTransactionToAbort, comsvcs/ICrmLogControl::ForceTransactionToAbort, cos.icrmlogcontrol_forcetransactiontoabort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmLogControl.ForceTransactionToAbort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmLogControl::ForceTransactionToAbort


## -description


Performs an immediate abort call on the transaction.


## -parameters






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
This method was called in the wrong state; either before <a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">RegisterCompensator</a> or when the transaction is completing (CRM Worker).

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




<a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a>
 

 

