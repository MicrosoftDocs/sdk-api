---
UID: NF:msrdc.IRdcLibrary.CreateSignatureReader
title: IRdcLibrary::CreateSignatureReader (msrdc.h)
description: Creates a signature reader to allow an application to decode the contents of a signature file.
helpviewer_keywords: ["CreateSignatureReader","CreateSignatureReader method [Remote Differential Compression]","CreateSignatureReader method [Remote Differential Compression]","IRdcLibrary interface","IRdcLibrary interface [Remote Differential Compression]","CreateSignatureReader method","IRdcLibrary.CreateSignatureReader","IRdcLibrary::CreateSignatureReader","fs.irdclibrary_createsignaturereader","msrdc/IRdcLibrary::CreateSignatureReader","rdc.irdclibrary_createsignaturereader"]
old-location: rdc\irdclibrary_createsignaturereader.htm
tech.root: rdc
ms.assetid: 08627c9d-7470-47ab-9209-32734082c393
ms.date: 12/05/2018
ms.keywords: CreateSignatureReader, CreateSignatureReader method [Remote Differential Compression], CreateSignatureReader method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],CreateSignatureReader method, IRdcLibrary.CreateSignatureReader, IRdcLibrary::CreateSignatureReader, fs.irdclibrary_createsignaturereader, msrdc/IRdcLibrary::CreateSignatureReader, rdc.irdclibrary_createsignaturereader
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
 - IRdcLibrary::CreateSignatureReader
 - msrdc/IRdcLibrary::CreateSignatureReader
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
 - IRdcLibrary.CreateSignatureReader
---

# IRdcLibrary::CreateSignatureReader


## -description

The <b>CreateSignatureReader</b> method 
    creates a signature reader to allow an application to decode the contents of a signature 
    file.

## -parameters

### -param iFileReader [in]

An <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a> interface pointer initialized to read the signatures.

### -param iSignatureReader [out]

Pointer to a location that will receive an 
    <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsignaturereader">IRdcSignatureReader</a> interface pointer. On a 
  successful return the interface will be initialized on return. Callers must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdclibrary">IRdcLibrary</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsignaturereader">IRdcSignatureReader</a>