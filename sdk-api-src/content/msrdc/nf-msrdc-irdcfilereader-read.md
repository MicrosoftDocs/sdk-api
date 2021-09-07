---
UID: NF:msrdc.IRdcFileReader.Read
title: IRdcFileReader::Read (msrdc.h)
description: Reads the specified amount of data starting at the specified position.
helpviewer_keywords: ["IRdcFileReader interface [Remote Differential Compression]","Read method","IRdcFileReader.Read","IRdcFileReader::Read","Read","Read method [Remote Differential Compression]","Read method [Remote Differential Compression]","IRdcFileReader interface","fs.irdcfilereader_read","msrdc/IRdcFileReader::Read","rdc.irdcfilereader_read"]
old-location: rdc\irdcfilereader_read.htm
tech.root: rdc
ms.assetid: 194944c8-94a8-4f9b-9970-012392e069b1
ms.date: 12/05/2018
ms.keywords: IRdcFileReader interface [Remote Differential Compression],Read method, IRdcFileReader.Read, IRdcFileReader::Read, Read, Read method [Remote Differential Compression], Read method [Remote Differential Compression],IRdcFileReader interface, fs.irdcfilereader_read, msrdc/IRdcFileReader::Read, rdc.irdcfilereader_read
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
 - IRdcFileReader::Read
 - msrdc/IRdcFileReader::Read
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
 - IRdcFileReader.Read
---

# IRdcFileReader::Read


## -description

The <b>Read</b> method reads the specified amount 
    of data starting at the specified position.

## -parameters

### -param offsetFileStart [in]

Offset from the start of the data at which to start the read.

### -param bytesToRead [in]

Number of bytes to be read.

### -param bytesActuallyRead [out]

Address of a <b>ULONG</b> that will receive the number of bytes read.

### -param buffer [out]

Address of the buffer that receives the data read. This buffer must be at least 
      <i>bytesToRead</i> bytes in size.

### -param eof [out]

Address of a <b>BOOL</b> that is set to <b>TRUE</b> if the end of 
      the file has been read.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Typically RDC will read the file sequentially from start to end. When reading signatures, the file may be read 
    more than once.

If the <b>BOOL</b> pointed to by the <i>eof</i> parameter is not <b>TRUE</b> 
    on return then the value pointed to by the <i>bytesActuallyRead</i> parameter must equal the 
    <i>bytesToRead</i> parameter. If the value pointed to by the <i>eof</i> 
    parameter is set, then the value pointed to by the <i>bytesActuallyRead</i> parameter can be 
    any value between zero and the <i>bytesToRead</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>