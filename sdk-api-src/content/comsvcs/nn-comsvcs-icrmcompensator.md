---
UID: NN:comsvcs.ICrmCompensator
title: ICrmCompensator
author: windows-sdk-content
description: Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.
old-location: cos\icrmcompensator.htm
tech.root: cossdk
ms.assetid: 9e5a8f2c-4115-42bd-a541-d0ce75c45b72
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ICrmCompensator, ICrmCompensator interface [COM+], ICrmCompensator interface [COM+],described, _dtc_ICrmCompensator_Interface, comsvcs/ICrmCompensator, cos.icrmcompensator
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmCompensator interface


## -description


Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmCompensator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICrmCompensator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/79dcf391-7ec9-4c9c-9f91-0e806d7c278c">AbortRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/443d0a09-0f5f-4237-870b-5cc47c80e2fe">BeginAbort</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/350f91f9-b019-4c70-9c3e-0d567479d3d0">BeginCommit</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the commit phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/316a9b00-5843-40b3-9c72-a71da21a81d0">BeginPrepare</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d444973d-d069-480e-b459-405057717776">CommitRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record in forward order during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/009209fe-0910-4db1-b5c2-accd7239c3e5">EndAbort</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has received all the log records available during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83701797-c386-4471-91ed-cbe936b1988e">EndCommit</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97dfdd8c-1a33-4173-aa71-cb9c9b1ef5ee">EndPrepare</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12b4d0d5-29f3-4fbb-8091-1b7d5ba0adb4">PrepareRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record in forward order during the prepare phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a68e49c7-a0d3-4c37-b438-864578e4a680">SetLogControl</a>
</td>
<td align="left" width="63%">
Delivers an <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface to the CRM Compensator so that it can write further log records during transaction completion.

</td>
</tr>
</table> 


## -remarks



The CRM clerk determines the CLSID of the CRM Compensator using the <a href="https://msdn.microsoft.com/f7907dff-a4a1-4526-8dab-547e819199ec">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> for both the <b>ICrmCompensator</b> interface and the <a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/3d490da6-1577-4a77-9f7d-6188f96f2914">COM+ Compensating Resource Manager</a>



<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

