---
UID: NF:msrdc.IRdcFileWriter.Write
title: IRdcFileWriter::Write (msrdc.h)
description: Write bytes to a file starting at a given offset.
helpviewer_keywords: ["IRdcFileWriter interface [Remote Differential Compression]","Write method","IRdcFileWriter.Write","IRdcFileWriter::Write","Write","Write method [Remote Differential Compression]","Write method [Remote Differential Compression]","IRdcFileWriter interface","fs.irdcfilewriter_write","msrdc/IRdcFileWriter::Write","rdc.irdcfilewriter_write"]
old-location: rdc\irdcfilewriter_write.htm
tech.root: rdc
ms.assetid: be7f3f2c-017a-4ca5-9652-a9b091c168be
ms.date: 12/05/2018
ms.keywords: IRdcFileWriter interface [Remote Differential Compression],Write method, IRdcFileWriter.Write, IRdcFileWriter::Write, Write, Write method [Remote Differential Compression], Write method [Remote Differential Compression],IRdcFileWriter interface, fs.irdcfilewriter_write, msrdc/IRdcFileWriter::Write, rdc.irdcfilewriter_write
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
 - IRdcFileWriter::Write
 - msrdc/IRdcFileWriter::Write
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
 - IRdcFileWriter.Write
---

# IRdcFileWriter::Write


## -description

Write bytes to a file starting at a given offset.

## -parameters

### -param offsetFileStart [in]

Starting offset.

### -param bytesToWrite [in]

Number of bytes to be written to the file.

### -param buffer [out]

The data to be written to the file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a>