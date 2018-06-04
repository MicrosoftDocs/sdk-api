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

# ICrmCompensator::PrepareRecord


## -description


Delivers a log record in forward order during the prepare phase. This method can be received by the CRM Compensator multiple times, once for each log record that is written.


## -parameters




### -param crmLogRec [in]

The log record, as a <a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a> structure.


### -param pfForget [out]

Indicates whether the delivered record should be forgotten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Unstructured log records are delivered as a <a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a> structure. In addition to the user data (as a single BLOB), this structure contains a couple of additional fields that might be useful for debugging or fault-finding if human compensation is necessary. The <b>dwCrmFlags</b> member is a bitfield that provides further information about whether this record was forgotten at some point and when it was written. The <b>dwSequenceNumber</b> member provides the sequence number of the log record. In most cases, sequence numbers are sequential but are not necessarily contiguous due to internal log records that are not delivered to the CRM Compensator.

If no log records are written by the CRM Worker, the <a href="https://msdn.microsoft.com/316a9b00-5843-40b3-9c72-a71da21a81d0">BeginPrepare</a> and <a href="https://msdn.microsoft.com/97dfdd8c-1a33-4173-aa71-cb9c9b1ef5ee">EndPrepare</a> methods are received but there are no <b>PrepareRecord</b> method calls. This is to allow for CRM Compensators that write log records at prepare time only.

The CRM Compensator can choose to forget the record that is delivered to it during this phase by setting the forget flag on return from this method.




## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>
 

 

