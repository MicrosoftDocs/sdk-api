---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

