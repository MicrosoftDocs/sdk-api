---
UID: NF:comsvcs.ICrmLogControl.RegisterCompensator
title: ICrmLogControl::RegisterCompensator (comsvcs.h)
description: The CRM Worker uses this method to register the CRM Compensator with the CRM infrastructure.
helpviewer_keywords: ["ICrmLogControl interface [COM+]","RegisterCompensator method","ICrmLogControl.RegisterCompensator","ICrmLogControl::RegisterCompensator","RegisterCompensator","RegisterCompensator method [COM+]","RegisterCompensator method [COM+]","ICrmLogControl interface","_dtc_ICrmLogControl_RegisterCompensator","comsvcs/ICrmLogControl::RegisterCompensator","cos.icrmlogcontrol_registercompensator"]
old-location: cos\icrmlogcontrol_registercompensator.htm
tech.root: cos
ms.assetid: f7907dff-a4a1-4526-8dab-547e819199ec
ms.date: 12/05/2018
ms.keywords: ICrmLogControl interface [COM+],RegisterCompensator method, ICrmLogControl.RegisterCompensator, ICrmLogControl::RegisterCompensator, RegisterCompensator, RegisterCompensator method [COM+], RegisterCompensator method [COM+],ICrmLogControl interface, _dtc_ICrmLogControl_RegisterCompensator, comsvcs/ICrmLogControl::RegisterCompensator, cos.icrmlogcontrol_registercompensator
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
 - ICrmLogControl::RegisterCompensator
 - comsvcs/ICrmLogControl::RegisterCompensator
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
 - ICrmLogControl.RegisterCompensator
---

# ICrmLogControl::RegisterCompensator


## -description

The CRM Worker uses this method to register the CRM Compensator with the CRM infrastructure. It must be the first method called by the CRM Worker, and it can be called successfully only once. If the CRM Worker receives a "recovery in progress" error code on calling this method, it should call this method again until it receives success.

## -parameters

### -param lpcwstrProgIdCompensator [in]

The ProgId of the CRM Compensator. The CLSID of the CRM Compensator in string form is also accepted.

### -param lpcwstrDescription [in]

The description string to be used by the monitoring interfaces.

### -param lCrmRegFlags [in]

Flags from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-crmregflags">CRMREGFLAGS</a> enumeration that control which phases of transaction completion should be received by the CRM Compensator and whether recovery should fail if in-doubt transactions remain after recovery has been attempted.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_NOTRANSACTION</b></dt>
</dl>
</td>
<td width="60%">
The component creating the CRM clerk does not have a transaction.

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
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_RECOVERY_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Recovery of the CRM log file failed because in-doubt transactions remain.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
An out of memory error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The CRM Compensator does not support at least one of the required interfaces (<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a> or <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>).


</td>
</tr>
</table>

## -remarks

The <i>lCrmRegFlags</i> parameter enables the implementer to decide which phases of transaction completion the CRM Compensator wants to receive. Some CRM Compensators might perform no work in the prepare phase and therefore have no need to receive prepare notifications; it can improve performance to specify that no prepare phase is required in this case.

It is recommended that CRM Workers and CRM Compensators be developed as "Both" threaded components (Threading Model = Any Apartment). However, in some cases this might not be possible due to language constraints (for example, when developing CRMs with Visual Basic). Apartment-threaded CRM Compensators (Threading Model = Single Thread Apartment) will deadlock in the prepare phase unless their synchronization property is set to "not supported". Another alternative for Apartment-threaded CRM Compensators is to skip the prepare phase if it is not necessary.

In scenarios with multiple Distributed Transaction Coordinators (DTCs), it is possible that a DTC transaction can go into the in-doubt state. Normally, this is because an interruption occurred during a transaction and the originator of the transaction cannot be contacted to find out the outcome of the transaction. In this case, the CRM infrastructure cannot determine the outcome of the transaction. A CRM implementer can decide whether new transactions should be allowed in this case.

The "fail if in-doubts remain" flag is used as follows: By specifying the "fail if in-doubts remain" flag on <b>RegisterCompensator</b>, if in-doubt transactions remain after recovery, the call to <b>RegisterCompensator</b> fails with a "recovery failed" error code. If the "fail if in-doubts remain" flag is not specified, the recovery succeeds, new transactions are allowed, and the in-doubt transactions remain in the CRM log file. The CRM infrastructure attempts to resolve these in-doubt transactions again on the next recovery (when the application server process is restarted).

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a>