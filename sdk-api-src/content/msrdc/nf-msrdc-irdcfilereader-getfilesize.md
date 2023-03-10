---
UID: NF:msrdc.IRdcFileReader.GetFileSize
title: IRdcFileReader::GetFileSize (msrdc.h)
description: Returns the size of a file.
helpviewer_keywords: ["GetFileSize","GetFileSize method [Remote Differential Compression]","GetFileSize method [Remote Differential Compression]","IRdcFileReader interface","IRdcFileReader interface [Remote Differential Compression]","GetFileSize method","IRdcFileReader.GetFileSize","IRdcFileReader::GetFileSize","fs.irdcfilereader_getfilesize","msrdc/IRdcFileReader::GetFileSize","rdc.irdcfilereader_getfilesize"]
old-location: rdc\irdcfilereader_getfilesize.htm
tech.root: rdc
ms.assetid: 2db66eb0-7213-446a-ad4b-f0df9e48abd4
ms.date: 12/05/2018
ms.keywords: GetFileSize, GetFileSize method [Remote Differential Compression], GetFileSize method [Remote Differential Compression],IRdcFileReader interface, IRdcFileReader interface [Remote Differential Compression],GetFileSize method, IRdcFileReader.GetFileSize, IRdcFileReader::GetFileSize, fs.irdcfilereader_getfilesize, msrdc/IRdcFileReader::GetFileSize, rdc.irdcfilereader_getfilesize
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
 - IRdcFileReader::GetFileSize
 - msrdc/IRdcFileReader::GetFileSize
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
 - IRdcFileReader.GetFileSize
---

# IRdcFileReader::GetFileSize


## -description

The <b>GetFileSize</b> method returns the 
    size of a file.

## -parameters

### -param fileSize [out]

Address of a <b>ULONGLONG</b> that on successful return will be filled with the size 
      of the file, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>