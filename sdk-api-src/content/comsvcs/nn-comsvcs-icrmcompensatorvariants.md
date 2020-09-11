---
UID: NN:comsvcs.ICrmCompensatorVariants
title: ICrmCompensatorVariants (comsvcs.h)
description: Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.
helpviewer_keywords: ["ICrmCompensatorVariants","ICrmCompensatorVariants interface [COM+]","ICrmCompensatorVariants interface [COM+]","described","_dtc_ICrmCompensatorVariants_Interface","comsvcs/ICrmCompensatorVariants","cos.icrmcompensatorvariants"]
old-location: cos\icrmcompensatorvariants.htm
tech.root: cos
ms.assetid: 44b80062-b2bb-4c34-b9e1-31229c8e40ca
ms.date: 12/05/2018
ms.keywords: ICrmCompensatorVariants, ICrmCompensatorVariants interface [COM+], ICrmCompensatorVariants interface [COM+],described, _dtc_ICrmCompensatorVariants_Interface, comsvcs/ICrmCompensatorVariants, cos.icrmcompensatorvariants
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
 - ICrmCompensatorVariants
 - comsvcs/ICrmCompensatorVariants
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
 - ICrmCompensatorVariants
---

# ICrmCompensatorVariants interface


## -description

Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmCompensatorVariants</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICrmCompensatorVariants</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICrmCompensatorVariants</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-abortrecordvariants">AbortRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-beginabortvariants">BeginAbortVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-begincommitvariants">BeginCommitVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the commit phase (phase two) of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-beginpreparevariants">BeginPrepareVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-commitrecordvariants">CommitRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-endabortvariants">EndAbortVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has received all the log records available during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-endcommitvariants">EndCommitVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-endpreparevariants">EndPrepareVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-preparerecordvariants">PrepareRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the prepare phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-setlogcontrolvariants">SetLogControlVariants</a>
</td>
<td align="left" width="63%">
Delivers an <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface to the CRM Compensator.


</td>
</tr>
</table>

## -remarks

The CRM clerk determines the CLSID of the CRM Compensator using the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for both the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a> interface and the <b>ICrmCompensatorVariants</b> interface.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--compensating-resource-manager">COM+ Compensating Resource Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>

