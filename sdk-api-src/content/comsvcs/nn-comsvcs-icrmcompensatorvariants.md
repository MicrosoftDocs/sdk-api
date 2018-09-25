---
UID: NN:comsvcs.ICrmCompensatorVariants
title: ICrmCompensatorVariants
author: windows-sdk-content
description: Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.
old-location: cos\icrmcompensatorvariants.htm
tech.root: cossdk
ms.assetid: 44b80062-b2bb-4c34-b9e1-31229c8e40ca
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICrmCompensatorVariants, ICrmCompensatorVariants interface [COM+], ICrmCompensatorVariants interface [COM+],described, _dtc_ICrmCompensatorVariants_Interface, comsvcs/ICrmCompensatorVariants, cos.icrmcompensatorvariants
ms.prod: windows
ms.technology: windows-sdk
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
 - ICrmCompensatorVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmCompensatorVariants interface


## -description


Delivers structured log records to the CRM Compensator when using Microsoft Visual Basic.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmCompensatorVariants</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICrmCompensatorVariants</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms685084(v=VS.85).aspx">AbortRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681202(v=VS.85).aspx">BeginAbortVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685165(v=VS.85).aspx">BeginCommitVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the commit phase (phase two) of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687798(v=VS.85).aspx">BeginPrepareVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680322(v=VS.85).aspx">CommitRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678830(v=VS.85).aspx">EndAbortVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has received all the log records available during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678945(v=VS.85).aspx">EndCommitVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679521(v=VS.85).aspx">EndPrepareVariants</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681728(v=VS.85).aspx">PrepareRecordVariants</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the prepare phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681730(v=VS.85).aspx">SetLogControlVariants</a>
</td>
<td align="left" width="63%">
Delivers an <a href="https://msdn.microsoft.com/en-us/library/ms679573(v=VS.85).aspx">ICrmLogControl</a> interface to the CRM Compensator.


</td>
</tr>
</table> 


## -remarks



The CRM clerk determines the CLSID of the CRM Compensator using the <a href="https://msdn.microsoft.com/en-us/library/ms688384(v=VS.85).aspx">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> for both the <a href="https://msdn.microsoft.com/en-us/library/ms685039(v=VS.85).aspx">ICrmCompensator</a> interface and the <b>ICrmCompensatorVariants</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680326(v=VS.85).aspx">COM+ Compensating Resource Manager</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685039(v=VS.85).aspx">ICrmCompensator</a>
 

 

