---
UID: NF:comsvcs.ICrmLogControl.get_TransactionUOW
title: ICrmLogControl::get_TransactionUOW method
author: windows-driver-content
description: Retrieves the transaction unit of work (UOW) without having to log the transaction UOW in the log record.
old-location: cos\icrmlogcontrol_get_transactionuow.htm
old-project: cossdk
ms.assetid: 35cfadf5-f1be-4383-bb34-f68543df0abb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ICrmLogControl, ICrmLogControl interface [COM+], get_TransactionUOW method, ICrmLogControl::get_TransactionUOW, _dtc_ICrmLogControl_TransactionUOW, comsvcs/ICrmLogControl::get_TransactionUOW, cos.icrmlogcontrol_get_transactionuow, get_TransactionUOW method [COM+], get_TransactionUOW method [COM+], ICrmLogControl interface, get_TransactionUOW,ICrmLogControl.get_TransactionUOW
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICrmLogControl.get_TransactionUOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmLogControl::get_TransactionUOW method


## -description


Retrieves the transaction unit of work (UOW) without having to log the transaction UOW in the log record.


## -parameters




### -param pVal [out]

The UOW of the transaction.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
An out of memory error has occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a>
 

 

