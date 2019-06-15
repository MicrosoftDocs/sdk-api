---
UID: NF:msrdc.IRdcFileWriter.Write
title: IRdcFileWriter::Write (msrdc.h)
author: windows-sdk-content
description: Write bytes to a file starting at a given offset.
old-location: rdc\irdcfilewriter_write.htm
tech.root: rdc
ms.assetid: be7f3f2c-017a-4ca5-9652-a9b091c168be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRdcFileWriter interface [Remote Differential Compression],Write method, IRdcFileWriter.Write, IRdcFileWriter::Write, Write, Write method [Remote Differential Compression], Write method [Remote Differential Compression],IRdcFileWriter interface, fs.irdcfilewriter_write, msrdc/IRdcFileWriter::Write, rdc.irdcfilewriter_write
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcFileWriter.Write
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a>
 

 

