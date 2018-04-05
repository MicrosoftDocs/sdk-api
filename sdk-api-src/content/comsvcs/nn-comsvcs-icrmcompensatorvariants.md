---
UID: NN:comsvcs.ICrmCompensatorVariants
title: ICrmCompensatorVariants
author: windows-driver-content
description: Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.
old-location: cos\icrmcompensatorvariants.htm
old-project: cossdk
ms.assetid: 44b80062-b2bb-4c34-b9e1-31229c8e40ca
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ICrmCompensatorVariants, ICrmCompensatorVariants interface [COM+], ICrmCompensatorVariants interface [COM+], described, _dtc_ICrmCompensatorVariants_Interface, comsvcs/ICrmCompensatorVariants, cos.icrmcompensatorvariants
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	ICrmCompensatorVariants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensatorVariants interface


## -description


Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmCompensatorVariants</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICrmCompensatorVariants</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a1ea366d-f3c6-4987-9f5b-32e3dd3e5d12">AbortRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/485170e3-c69b-446a-af93-a0ed4f25c84a">BeginAbortVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6cd7421-5173-4edb-b752-5fbc44bac6dc">BeginCommitVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the commit phase (phase two) of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0cbfc39-2a29-4b1f-8d6e-87d0b1c68582">BeginPrepareVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d3ae282-d2cd-48cf-a093-c8f5ef9cc29a">CommitRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/021880c3-e52c-4fa7-9815-3180ee1564da">EndAbortVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has received all the log records available during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1004437b-0281-439c-9b6d-0043caeb2844">EndCommitVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b9a7e75-5e7c-4f5b-b625-78abb3c5e9b7">EndPrepareVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cbe3bf9-b82c-42da-ac19-dddb5837368e">PrepareRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the prepare phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cf602fb-b5b9-471b-b617-9df6725eaf35">SetLogControlVariants</a>
</td>
<td align="left" width="63%">
Delivers an <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface to the CRM Compensator.


</td>
</tr>
</table> 


## -remarks



The CRM clerk determines the CLSID of the CRM Compensator using the <a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for both the <a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a> interface and the <b>ICrmCompensatorVariants</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/3d490da6-1577-4a77-9f7d-6188f96f2914">COM+ Compensating Resource Manager</a>



<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

