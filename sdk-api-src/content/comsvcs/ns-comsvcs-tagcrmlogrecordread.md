---
UID: NS:comsvcs.tagCrmLogRecordRead
title: tagCrmLogRecordRead
author: windows-driver-content
description: Contains unstructured log records for the Compensating Resource Manager (CRM).
old-location: cos\crmlogrecordread.htm
old-project: cossdk
ms.assetid: 0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: CrmLogRecordRead, CrmLogRecordRead structure [COM+], _cos_CrmLogRecordRead, comsvcs/CrmLogRecordRead, cos.crmlogrecordread, tagCrmLogRecordRead
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CrmLogRecordRead
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ComSvcs.h
api_name:
-	CrmLogRecordRead
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagCrmLogRecordRead structure


## -description


Contains unstructured log records for the Compensating Resource Manager (CRM).


## -struct-fields




### -field dwCrmFlags

Information about when this record was written. For a list of values, see <a href="https://msdn.microsoft.com/ef41c99c-9f57-430f-af43-ba0ee1eb7a03">CRMFLAGS</a>.


### -field dwSequenceNumber

The sequence number of the log record. Sequence numbers are not necessarily contiguous because not all internal log records or forgotten log records are delivered to the CRM Compensator.


### -field blobUserData

The user data.


## -see-also




<a href="https://msdn.microsoft.com/9e5a8f2c-4115-42bd-a541-d0ce75c45b72">ICrmCompensator</a>



<a href="https://msdn.microsoft.com/aa801bd0-5253-4f9f-8859-b808d4dc081b">ICrmFormatLogRecords</a>
 

 

