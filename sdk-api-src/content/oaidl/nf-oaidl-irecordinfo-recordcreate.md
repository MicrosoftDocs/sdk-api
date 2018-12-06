---
UID: NF:oaidl.IRecordInfo.RecordCreate
title: IRecordInfo::RecordCreate
author: windows-sdk-content
description: Allocates memory for a new record, initializes the instance and returns a pointer to the record.
old-location: automat\irecordinfo_recordcreate.htm
tech.root: automat
ms.assetid: f688623e-c03b-456f-bd51-426049e0eb2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRecordInfo interface [Automation],RecordCreate method, IRecordInfo.RecordCreate, IRecordInfo::RecordCreate, RecordCreate, RecordCreate method [Automation], RecordCreate method [Automation],IRecordInfo interface, _oa96_IRecordInfo_RecordCreate, automat.irecordinfo_recordcreate, oaidl/IRecordInfo::RecordCreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - oaidl.h
api_name:
 - IRecordInfo.RecordCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRecordInfo::RecordCreate


## -description


Allocates memory for a new record, initializes the instance and returns a pointer to the record.


## -parameters






## -returns



This method returns a pointer to the created record.




## -remarks



The memory is set to zeros before it is returned. 

The records created must be freed by calling <a href="https://msdn.microsoft.com/36faf2f6-ecb5-4d6f-a05d-a37ae21a8f07">RecordDestroy</a>.




## -see-also




<a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a>
 

 

