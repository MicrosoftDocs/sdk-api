---
UID: NN:comsvcs.ICrmCompensator
title: ICrmCompensator
author: windows-sdk-content
description: Delivers unstructured log records to the CRM Compensator when using Microsoft Visual C++.
old-location: cos\icrmcompensator.htm
tech.root: cossdk
ms.assetid: 9e5a8f2c-4115-42bd-a541-d0ce75c45b72
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICrmCompensator, ICrmCompensator interface [COM+], ICrmCompensator interface [COM+],described, _dtc_ICrmCompensator_Interface, comsvcs/ICrmCompensator, cos.icrmcompensator
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmCompensator</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICrmCompensator</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms682810(v=VS.85).aspx">AbortRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record to the CRM Compensator during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680651(v=VS.85).aspx">BeginAbort</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679823(v=VS.85).aspx">BeginCommit</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the commit phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679561(v=VS.85).aspx">BeginPrepare</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686784(v=VS.85).aspx">CommitRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record in forward order during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678824(v=VS.85).aspx">EndAbort</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has received all the log records available during the abort phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683528(v=VS.85).aspx">EndCommit</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684319(v=VS.85).aspx">EndPrepare</a>
</td>
<td align="left" width="63%">
Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678961(v=VS.85).aspx">PrepareRecord</a>
</td>
<td align="left" width="63%">
Delivers a log record in forward order during the prepare phase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685163(v=VS.85).aspx">SetLogControl</a>
</td>
<td align="left" width="63%">
Delivers an <a href="https://msdn.microsoft.com/en-us/library/ms679573(v=VS.85).aspx">ICrmLogControl</a> interface to the CRM Compensator so that it can write further log records during transaction completion.

</td>
</tr>
</table> 


## -remarks



The CRM clerk determines the CLSID of the CRM Compensator using the <a href="https://msdn.microsoft.com/en-us/library/ms688384(v=VS.85).aspx">ICrmLogControl::RegisterCompensator</a> method. It next calls <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> specifying the CLSID of this CRM Compensator, and then it calls <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> for both the <b>ICrmCompensator</b> interface and the <a href="https://msdn.microsoft.com/en-us/library/ms680662(v=VS.85).aspx">ICrmCompensatorVariants</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680326(v=VS.85).aspx">COM+ Compensating Resource Manager</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680662(v=VS.85).aspx">ICrmCompensatorVariants</a>
 

 

