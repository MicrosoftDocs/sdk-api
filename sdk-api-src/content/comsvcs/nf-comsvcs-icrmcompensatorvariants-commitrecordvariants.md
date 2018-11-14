---
UID: NF:comsvcs.ICrmCompensatorVariants.CommitRecordVariants
title: ICrmCompensatorVariants::CommitRecordVariants
author: windows-sdk-content
description: Delivers a log record to the CRM Compensator during the commit phase.
old-location: cos\icrmcompensatorvariants_commitrecordvariants.htm
tech.root: cossdk
ms.assetid: 3d3ae282-d2cd-48cf-a093-c8f5ef9cc29a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CommitRecordVariants, CommitRecordVariants method [COM+], CommitRecordVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],CommitRecordVariants method, ICrmCompensatorVariants.CommitRecordVariants, ICrmCompensatorVariants::CommitRecordVariants, _dtc_ICrmCompensatorVariants_CommitRecordVariants, comsvcs/ICrmCompensatorVariants::CommitRecordVariants, cos.icrmcompensatorvariants_commitrecordvariants
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
 - ICrmCompensatorVariants.CommitRecordVariants
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
- ICrmCompensatorVariants.CommitRecordVariants
: 
---

# ICrmCompensatorVariants::CommitRecordVariants


## -description


Delivers a log record to the CRM Compensator during the commit phase. Log records are delivered in the order in which they were written.


## -parameters




### -param pLogRecord [in]

The log record (as a Variant array of Variants).


### -param pbForget [out]

Indicates whether the delivered record should be forgotten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be received by the CRM Compensator multiple times, once for each log record that is written. If no log records are written, the <a href="https://msdn.microsoft.com/a6cd7421-5173-4edb-b752-5fbc44bac6dc">BeginCommitVariants</a> and <a href="https://msdn.microsoft.com/1004437b-0281-439c-9b6d-0043caeb2844">EndCommitVariants</a> methods are received but there are no <b>CommitRecordVariants</b> method calls.

The CRM Compensator can choose to forget the record that is delivered to it during this method by setting the forget flag on return from this method.




## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

