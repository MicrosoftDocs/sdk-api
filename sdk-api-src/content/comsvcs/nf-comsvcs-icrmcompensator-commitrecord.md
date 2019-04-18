---
UID: NF:comsvcs.ICrmCompensator.CommitRecord
title: ICrmCompensator::CommitRecord (comsvcs.h)
author: windows-sdk-content
description: Delivers a log record in forward order during the commit phase.
old-location: cos\icrmcompensator_commitrecord.htm
tech.root: cossdk
ms.assetid: d444973d-d069-480e-b459-405057717776
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CommitRecord, CommitRecord method [COM+], CommitRecord method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],CommitRecord method, ICrmCompensator.CommitRecord, ICrmCompensator::CommitRecord, _dtc_ICrmCompensator_CommitRecord, comsvcs/ICrmCompensator::CommitRecord, cos.icrmcompensator_commitrecord
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
 - ICrmCompensator.CommitRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmCompensator::CommitRecord


## -description


Delivers a log record in forward order during the commit phase.


## -parameters




### -param crmLogRec [in]

The log record, as a <a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a> structure.


### -param pfForget [out]

Indicates whether the delivered record should be forgotten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be received by the CRM Compensator multiple times, once for each log record that is written. If no log records are written, the <a href="https://msdn.microsoft.com/350f91f9-b019-4c70-9c3e-0d567479d3d0">BeginCommit</a> and <a href="https://msdn.microsoft.com/83701797-c386-4471-91ed-cbe936b1988e">EndCommit</a> methods are received but there are no <b>CommitRecord</b> method calls.

The CRM Compensator can choose to forget the record that was delivered to it during this phase by setting the forget flag on return from this method.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

