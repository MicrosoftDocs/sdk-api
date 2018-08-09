---
UID: NF:comsvcs.ICrmCompensatorVariants.PrepareRecordVariants
title: ICrmCompensatorVariants::PrepareRecordVariants
author: windows-sdk-content
description: Delivers a log record to the CRM Compensator during the prepare phase.
old-location: cos\icrmcompensatorvariants_preparerecordvariants.htm
old-project: cossdk
ms.assetid: 5cbe3bf9-b82c-42da-ac19-dddb5837368e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICrmCompensatorVariants interface [COM+],PrepareRecordVariants method, ICrmCompensatorVariants.PrepareRecordVariants, ICrmCompensatorVariants::PrepareRecordVariants, PrepareRecordVariants, PrepareRecordVariants method [COM+], PrepareRecordVariants method [COM+],ICrmCompensatorVariants interface, _dtc_ICrmCompensatorVariants_PrepareRecordVariants, comsvcs/ICrmCompensatorVariants::PrepareRecordVariants, cos.icrmcompensatorvariants_preparerecordvariants
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmCompensatorVariants.PrepareRecordVariants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensatorVariants::PrepareRecordVariants


## -description


Delivers a log record to the CRM Compensator during the prepare phase. Log records are delivered in the order in which they were written.


## -parameters




### -param pLogRecord [in]

The log record (as a <b>Variant</b> array of <b>Variants</b>).


### -param pbForget [out]

Indicates whether the delivered record should be forgotten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can be received by the CRM Compensator multiple times, once for each log record that is written.

For the <a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a> interface, log records are delivered in the same way that they were written. The CRM flags and sequence number are appended as the last two elements in the array. (See <b>ICrmCompensator::PrepareRecord</b>.)

If no log records are written by the CRM Worker, the <a href="https://msdn.microsoft.com/f0cbfc39-2a29-4b1f-8d6e-87d0b1c68582">BeginPrepareVariants</a> and <a href="https://msdn.microsoft.com/2b9a7e75-5e7c-4f5b-b625-78abb3c5e9b7">EndPrepareVariants</a> methods are received by the CRM Compensator but there are no <b>PrepareRecordVariants</b> method calls. This is to allow for CRM Compensators that write log records at prepare time only.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.




## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

