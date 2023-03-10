---
UID: NF:msrdc.ISimilarity.GetRecordCount
title: ISimilarity::GetRecordCount (msrdc.h)
description: Retrieves the number of records that are stored in the similarity file ID table in a similarity file.
helpviewer_keywords: ["GetRecordCount","GetRecordCount method [Remote Differential Compression]","GetRecordCount method [Remote Differential Compression]","ISimilarity interface","ISimilarity interface [Remote Differential Compression]","GetRecordCount method","ISimilarity.GetRecordCount","ISimilarity::GetRecordCount","fs.isimilarity_getrecordcount","msrdc/ISimilarity::GetRecordCount","rdc.isimilarity_getrecordcount"]
old-location: rdc\isimilarity_getrecordcount.htm
tech.root: rdc
ms.assetid: 19dda0ed-0f11-4e17-823b-667a48cf6dc1
ms.date: 12/05/2018
ms.keywords: GetRecordCount, GetRecordCount method [Remote Differential Compression], GetRecordCount method [Remote Differential Compression],ISimilarity interface, ISimilarity interface [Remote Differential Compression],GetRecordCount method, ISimilarity.GetRecordCount, ISimilarity::GetRecordCount, fs.isimilarity_getrecordcount, msrdc/ISimilarity::GetRecordCount, rdc.isimilarity_getrecordcount
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarity::GetRecordCount
 - msrdc/ISimilarity::GetRecordCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarity.GetRecordCount
---

# ISimilarity::GetRecordCount


## -description

Retrieves the number of records that are stored in the similarity file ID table in a similarity file.

## -parameters

### -param recordCount [out]

A pointer to a variable that receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilarity">ISimilarity</a>