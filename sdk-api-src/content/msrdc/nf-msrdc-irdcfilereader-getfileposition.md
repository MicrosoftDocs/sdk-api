---
UID: NF:msrdc.IRdcFileReader.GetFilePosition
title: IRdcFileReader::GetFilePosition (msrdc.h)
description: Returns the current file position.
helpviewer_keywords: ["GetFilePosition","GetFilePosition method [Remote Differential Compression]","GetFilePosition method [Remote Differential Compression]","IRdcFileReader interface","IRdcFileReader interface [Remote Differential Compression]","GetFilePosition method","IRdcFileReader.GetFilePosition","IRdcFileReader::GetFilePosition","fs.irdcfilereader_getfileposition","msrdc/IRdcFileReader::GetFilePosition","rdc.irdcfilereader_getfileposition"]
old-location: rdc\irdcfilereader_getfileposition.htm
tech.root: rdc
ms.assetid: 3cef6883-29d2-4970-9a96-3500b58449d2
ms.date: 12/05/2018
ms.keywords: GetFilePosition, GetFilePosition method [Remote Differential Compression], GetFilePosition method [Remote Differential Compression],IRdcFileReader interface, IRdcFileReader interface [Remote Differential Compression],GetFilePosition method, IRdcFileReader.GetFilePosition, IRdcFileReader::GetFilePosition, fs.irdcfilereader_getfileposition, msrdc/IRdcFileReader::GetFilePosition, rdc.irdcfilereader_getfileposition
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
req.type-library: MsRdc.dll
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcFileReader::GetFilePosition
 - msrdc/IRdcFileReader::GetFilePosition
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
 - IRdcFileReader.GetFilePosition
---

# IRdcFileReader::GetFilePosition


## -description

The <b>GetFilePosition</b> method 
    returns the current file position.

## -parameters

### -param offsetFromStart [out]

Address of a <b>ULONGLONG</b> that will receive the current offset from the start of 
      the data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>