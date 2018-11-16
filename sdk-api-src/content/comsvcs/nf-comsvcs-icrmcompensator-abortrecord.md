---
UID: NF:comsvcs.ICrmCompensator.AbortRecord
title: ICrmCompensator::AbortRecord
author: windows-sdk-content
description: Delivers a log record to the CRM Compensator during the abort phase.
old-location: cos\icrmcompensator_abortrecord.htm
tech.root: cossdk
ms.assetid: 79dcf391-7ec9-4c9c-9f91-0e806d7c278c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AbortRecord, AbortRecord method [COM+], AbortRecord method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],AbortRecord method, ICrmCompensator.AbortRecord, ICrmCompensator::AbortRecord, _dtc_ICrmCompensator_AbortRecord, comsvcs/ICrmCompensator::AbortRecord, cos.icrmcompensator_abortrecord
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
 - ICrmCompensator.AbortRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- ICrmCompensator.AbortRecord
: 
---

# ICrmCompensator::AbortRecord


## -description


Delivers a log record to the CRM Compensator during the abort phase.


## -parameters




### -param crmLogRec [in]

The log record, as a <a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a> structure.


### -param pfForget [out]

Indicates whether the delivered record should be forgotten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Log records are delivered in the reverse order in which they were written. This method can be received by the CRM Compensator multiple times, once for each log record that was written. If no log records are written, the <a href="https://msdn.microsoft.com/443d0a09-0f5f-4237-870b-5cc47c80e2fe">BeginAbort</a> and <a href="https://msdn.microsoft.com/009209fe-0910-4db1-b5c2-accd7239c3e5">EndAbort</a> methods are received but there are no <b>AbortRecord</b> method calls.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

