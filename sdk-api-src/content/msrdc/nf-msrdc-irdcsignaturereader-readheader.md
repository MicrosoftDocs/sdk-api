---
UID: NF:msrdc.IRdcSignatureReader.ReadHeader
title: IRdcSignatureReader::ReadHeader (msrdc.h)
description: Reads the signature header and returns a copy of the parameters used to generate the signatures.
helpviewer_keywords: ["IRdcSignatureReader interface [Remote Differential Compression]","ReadHeader method","IRdcSignatureReader.ReadHeader","IRdcSignatureReader::ReadHeader","ReadHeader","ReadHeader method [Remote Differential Compression]","ReadHeader method [Remote Differential Compression]","IRdcSignatureReader interface","fs.irdcsignaturereader_readheader","msrdc/IRdcSignatureReader::ReadHeader","rdc.irdcsignaturereader_readheader"]
old-location: rdc\irdcsignaturereader_readheader.htm
tech.root: rdc
ms.assetid: c0f4d31d-338f-49fc-9f1a-e8e31ffa1bc7
ms.date: 12/05/2018
ms.keywords: IRdcSignatureReader interface [Remote Differential Compression],ReadHeader method, IRdcSignatureReader.ReadHeader, IRdcSignatureReader::ReadHeader, ReadHeader, ReadHeader method [Remote Differential Compression], ReadHeader method [Remote Differential Compression],IRdcSignatureReader interface, fs.irdcsignaturereader_readheader, msrdc/IRdcSignatureReader::ReadHeader, rdc.irdcsignaturereader_readheader
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
 - IRdcSignatureReader::ReadHeader
 - msrdc/IRdcSignatureReader::ReadHeader
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
 - IRdcSignatureReader.ReadHeader
---

# IRdcSignatureReader::ReadHeader


## -description

The 
   <b>ReadHeader</b> method
   reads the signature header and returns a copy of the parameters
   used to generate the signatures.

## -parameters

### -param rdc_ErrorCode [out]

Address of a <a href="/windows/win32/api/msrdc/ne-msrdc-rdc_errorcode">RDC_ErrorCode</a> enumeration that will 
      receive any RDC-specific error code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcsignaturereader">IRdcSignatureReader</a>



<a href="/windows/win32/api/msrdc/ne-msrdc-rdc_errorcode">RDC_ErrorCode</a>