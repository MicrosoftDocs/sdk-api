---
UID: NN:msrdc.IRdcFileReader
title: IRdcFileReader (msrdc.h)
description: The IRdcFileReader interface is used to provide the equivalent of a file handle, because the data being synchronized may not exist as a file on disk.
helpviewer_keywords: ["IRdcFileReader","IRdcFileReader interface [Remote Differential Compression]","IRdcFileReader interface [Remote Differential Compression]","described","fs.irdcfilereader","msrdc/IRdcFileReader","rdc.irdcfilereader"]
old-location: rdc\irdcfilereader.htm
tech.root: rdc
ms.assetid: 9684efca-37fd-45ce-a24e-d5276b8ea6af
ms.date: 12/05/2018
ms.keywords: IRdcFileReader, IRdcFileReader interface [Remote Differential Compression], IRdcFileReader interface [Remote Differential Compression],described, fs.irdcfilereader, msrdc/IRdcFileReader, rdc.irdcfilereader
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
 - IRdcFileReader
 - msrdc/IRdcFileReader
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
 - IRdcFileReader
---

# IRdcFileReader interface


## -description

The <b>IRdcFileReader</b> interface is used to provide the 
    equivalent of a file handle, because the data being synchronized may not exist as a file on disk.

## -inheritance

The <b>IRdcFileReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRdcFileReader</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-createcomparator">IRdcLibrary::CreateComparator</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdclibrary-createsignaturereader">IRdcLibrary::CreateSignatureReader</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-interfaces">Remote Differential Compression Interfaces</a>
