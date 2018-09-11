---
UID: NF:comsvcs.ICrmCompensatorVariants.AbortRecordVariants
title: ICrmCompensatorVariants::AbortRecordVariants
author: windows-sdk-content
description: Delivers a log record to the CRM Compensator during the abort phase.
old-location: cos\icrmcompensatorvariants_abortrecordvariants.htm
tech.root: cossdk
ms.assetid: a1ea366d-f3c6-4987-9f5b-32e3dd3e5d12
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AbortRecordVariants, AbortRecordVariants method [COM+], AbortRecordVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],AbortRecordVariants method, ICrmCompensatorVariants.AbortRecordVariants, ICrmCompensatorVariants::AbortRecordVariants, _dtc_ICrmCompensatorVariants_AbortRecordVariants, comsvcs/ICrmCompensatorVariants::AbortRecordVariants, cos.icrmcompensatorvariants_abortrecordvariants
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
 - ICrmCompensatorVariants.AbortRecordVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICrmCompensatorVariants::AbortRecordVariants


## -description


Delivers a log record to the CRM Compensator during the abort phase.


## -parameters




### -param pLogRecord [in]

The log record (as a <b>Variant</b> array of <b>Variants</b>).


### -param pbForget [out]

Indicates whether the delivered record should be forgotten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method may be received by the CRM Compensator multiple times, once for each log record that is written. If no log records are written, the <a href="https://msdn.microsoft.com/485170e3-c69b-446a-af93-a0ed4f25c84a">BeginAbortVariants</a> and <a href="https://msdn.microsoft.com/021880c3-e52c-4fa7-9815-3180ee1564da">EndAbortVariants</a> methods are received but there are no <b>AbortRecordVariants</b> method calls.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.




## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

