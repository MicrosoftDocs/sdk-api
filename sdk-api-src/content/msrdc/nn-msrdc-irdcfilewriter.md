---
UID: NN:msrdc.IRdcFileWriter
title: IRdcFileWriter (msrdc.h)
description: Abstract interface to read from and write to a file.
helpviewer_keywords: ["IRdcFileWriter","IRdcFileWriter interface [Remote Differential Compression]","IRdcFileWriter interface [Remote Differential Compression]","described","fs.irdcfilewriter","msrdc/IRdcFileWriter","rdc.irdcfilewriter"]
old-location: rdc\irdcfilewriter.htm
tech.root: rdc
ms.assetid: 8b6ac8d0-37fd-4bd3-aa44-5b57f546364d
ms.date: 12/05/2018
ms.keywords: IRdcFileWriter, IRdcFileWriter interface [Remote Differential Compression], IRdcFileWriter interface [Remote Differential Compression],described, fs.irdcfilewriter, msrdc/IRdcFileWriter, rdc.irdcfilewriter
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
 - IRdcFileWriter
 - msrdc/IRdcFileWriter
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
 - IRdcFileWriter
---

# IRdcFileWriter interface


## -description

Abstract interface to read from and write to a file.

The RDC application must implement this interface for use with <a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-createtableindirect">ISimilarityFileIdTable::CreateTableIndirect</a>. Note that this interface does not include methods to open, close, or flush the file to disk. The application is responsible for properly opening and closing the file represented by an instance of this interface.

## -inheritance

The <b>IRdcFileWriter</b> interface inherits from <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> and <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>. <b>IRdcFileWriter</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
