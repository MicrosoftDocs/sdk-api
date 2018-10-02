---
UID: NF:comsvcs.ICrmLogControl.WriteLogRecordVariants
title: ICrmLogControl::WriteLogRecordVariants
author: windows-sdk-content
description: The CRM Worker and CRM Compensator use this method to write structured log records to the log.
old-location: cos\icrmlogcontrol_writelogrecordvariants.htm
tech.root: cossdk
ms.assetid: ebd3943d-0c77-49fe-a53e-bc0c45e13a54
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICrmLogControl interface [COM+],WriteLogRecordVariants method, ICrmLogControl.WriteLogRecordVariants, ICrmLogControl::WriteLogRecordVariants, WriteLogRecordVariants, WriteLogRecordVariants method [COM+], WriteLogRecordVariants method [COM+],ICrmLogControl interface, _dtc_ICrmLogControl_WriteLogRecordVariants, comsvcs/ICrmLogControl::WriteLogRecordVariants, cos.icrmlogcontrol_writelogrecordvariants
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
 - ICrmLogControl.WriteLogRecordVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmLogControl::WriteLogRecordVariants


## -description


The CRM Worker and CRM Compensator use this method to write structured log records to the log.


## -parameters




### -param pLogRecord [in]

A pointer to a <b>Variant</b> array of <b>Variants</b>. This must be a single-dimension array whose lower bound is zero.


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
 

 

