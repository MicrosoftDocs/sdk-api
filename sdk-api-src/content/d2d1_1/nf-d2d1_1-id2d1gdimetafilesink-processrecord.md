---
UID: NF:d2d1_1.ID2D1GdiMetafileSink.ProcessRecord
title: ID2D1GdiMetafileSink::ProcessRecord
author: windows-sdk-content
description: This method is called once for each record stored in a metafile.
old-location: direct2d\id2d1gdimetafilesink_processrecord.htm
tech.root: direct2d
ms.assetid: E2133C62-A689-4FE6-8E9D-39E161EEFCE1
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1GdiMetafileSink interface [Direct2D],ProcessRecord method, ID2D1GdiMetafileSink.ProcessRecord, ID2D1GdiMetafileSink::ProcessRecord, ProcessRecord, ProcessRecord method [Direct2D], ProcessRecord method [Direct2D],ID2D1GdiMetafileSink interface, d2d1_1/ID2D1GdiMetafileSink::ProcessRecord, direct2d.id2d1gdimetafilesink_processrecord
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GdiMetafileSink.ProcessRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1GdiMetafileSink.ProcessRecord
: 
---

# ID2D1GdiMetafileSink::ProcessRecord


## -description


 This method is called once for each record stored in a metafile.


## -parameters




### -param recordType

Type: <b>DWORD</b>

The type of the record.


### -param recordData [out]

Type: <b>void*</b>

The data for the record.


### -param recordDataSize

Type: <b>UINT</b>

The byte size of the record data.


## -returns



Type: <b>BOOL</b>

Return true if the record is successfully.




## -see-also




<a href="https://msdn.microsoft.com/1E9866C3-2A07-48C2-A4C5-F9AE3C7B2272">ID2D1GdiMetafileSink</a>
 

 

