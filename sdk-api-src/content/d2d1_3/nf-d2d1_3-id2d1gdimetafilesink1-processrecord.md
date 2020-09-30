---
UID: NF:d2d1_3.ID2D1GdiMetafileSink1.ProcessRecord
title: ID2D1GdiMetafileSink1::ProcessRecord (d2d1_3.h)
description: Provides access to metafile records, including their type, data, and flags.
helpviewer_keywords: ["ID2D1GdiMetafileSink1 interface [Direct2D]","ProcessRecord method","ID2D1GdiMetafileSink1.ProcessRecord","ID2D1GdiMetafileSink1::ProcessRecord","ProcessRecord","ProcessRecord method [Direct2D]","ProcessRecord method [Direct2D]","ID2D1GdiMetafileSink1 interface","d2d1_3/ID2D1GdiMetafileSink1::ProcessRecord","direct2d.id2d1gdimetafilesink1_processrecord"]
old-location: direct2d\id2d1gdimetafilesink1_processrecord.htm
tech.root: Direct2D
ms.assetid: 1f33988f-e4c5-23f9-899a-64ebeaa77007
ms.date: 12/05/2018
ms.keywords: ID2D1GdiMetafileSink1 interface [Direct2D],ProcessRecord method, ID2D1GdiMetafileSink1.ProcessRecord, ID2D1GdiMetafileSink1::ProcessRecord, ProcessRecord, ProcessRecord method [Direct2D], ProcessRecord method [Direct2D],ID2D1GdiMetafileSink1 interface, d2d1_3/ID2D1GdiMetafileSink1::ProcessRecord, direct2d.id2d1gdimetafilesink1_processrecord
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GdiMetafileSink1::ProcessRecord
 - d2d1_3/ID2D1GdiMetafileSink1::ProcessRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GdiMetafileSink1.ProcessRecord
---

# ID2D1GdiMetafileSink1::ProcessRecord


## -description

Provides access to metafile records, including their type, data, and flags.

## -parameters

### -param recordType

Type: <b>DWORD</b>

The type of metafile record being processed. Please see <a href="/openspecs/windows_protocols/ms-emf/91c257d7-c39d-4a36-9b1f-63e3f73d30ca">MS-EMF</a> and <a href="/openspecs/windows_protocols/ms-emfplus/5f92c789-64f2-46b5-9ed4-15a9bb0946c6">MS-EMFPLUS</a> for a list of record types.

### -param recordData [in, optional]

Type: <b>const void*</b>

The data contained in this record. Please see <a href="/openspecs/windows_protocols/ms-emf/91c257d7-c39d-4a36-9b1f-63e3f73d30ca">MS-EMF</a> and <a href="/openspecs/windows_protocols/ms-emfplus/5f92c789-64f2-46b5-9ed4-15a9bb0946c6">MS-EMFPLUS</a> for information on record data layouts.

### -param recordDataSize

Type: <b>UINT</b>

TThe size of the data pointed to by recordData.

### -param flags

Type: <b>UINT32</b>

The set of flags set for this record. Please see <a href="/openspecs/windows_protocols/ms-emf/91c257d7-c39d-4a36-9b1f-63e3f73d30ca">MS-EMF</a> and <a href="/openspecs/windows_protocols/ms-emfplus/5f92c789-64f2-46b5-9ed4-15a9bb0946c6">MS-EMFPLUS</a> for information on record flags.

## -returns

Type: <b>HRESULT</b>

S_OK if successful, otherwise a failure HRESULT.

## -remarks

For details on the EMF and EMF+ formats, please see Microsoft technical documents  <a href="/openspecs/windows_protocols/ms-emf/91c257d7-c39d-4a36-9b1f-63e3f73d30ca">MS-EMF</a> and <a href="/openspecs/windows_protocols/ms-emfplus/5f92c789-64f2-46b5-9ed4-15a9bb0946c6">MS-EMFPLUS</a>.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gdimetafilesink">ID2D1GdiMetafileSink1</a>



<a href="/openspecs/windows_protocols/ms-emfplus/5f92c789-64f2-46b5-9ed4-15a9bb0946c6">[MS-EMFPLUS]: Enhanced Metafile Format Plus Extensions</a>



<a href="/openspecs/windows_protocols/ms-emf/91c257d7-c39d-4a36-9b1f-63e3f73d30ca">[MS-EMF]: Enhanced Metafile Format</a>