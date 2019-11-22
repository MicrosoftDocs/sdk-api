---
UID: NN:comsvcs.ICrmCompensator
title: ICrmCompensator (comsvcs.h)

description: Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.
old-location: cos\icrmcompensator.htm
tech.root: cossdk
ms.assetid: 9e5a8f2c-4115-42bd-a541-d0ce75c45b72

ms.date: 12/05/2018
ms.keywords: ICrmCompensator, ICrmCompensator interface [COM+], ICrmCompensator interface [COM+],described, _dtc_ICrmCompensator_Interface, comsvcs/ICrmCompensator, cos.icrmcompensator
ms.topic: interface
f1_keywords: 
 - "comsvcs/ICrmCompensator"
dev_langs:
 - c++
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
 - ICrmCompensator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmCompensator interface


## -description


Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmCompensator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICrmCompensator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICrmCompensator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-abortrecord">AbortRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-beginabort">BeginAbort</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-begincommit">BeginCommit</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the commit phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-beginprepare">BeginPrepare</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-commitrecord">CommitRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record in forward order during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-endabort">EndAbort</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has received all the log records available during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-endcommit">EndCommit</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-endprepare">EndPrepare</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-preparerecord">PrepareRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record in forward order during the prepare phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensator-setlogcontrol">SetLogControl</a>
</td>
<td align="left" width="63%">
Delivers an <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface to the CRM Compensator so that it can write further log records during transaction completion.

</td>
</tr>
</table> 


## -remarks



The CRM clerk determines the CLSID of the CRM Compensator using the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icrmlogcontrol-registercompensator">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> for both the <b>ICrmCompensator</b> interface and the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--compensating-resource-manager">COM+ Compensating Resource Manager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
 

 

