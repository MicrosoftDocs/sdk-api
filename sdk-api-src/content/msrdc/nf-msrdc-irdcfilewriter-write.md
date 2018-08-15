---
UID: NF:msrdc.IRdcFileWriter.Write
title: IRdcFileWriter::Write
author: windows-sdk-content
description: Write bytes to a file starting at a given offset.
old-location: rdc\irdcfilewriter_write.htm
old-project: Rdc
ms.assetid: be7f3f2c-017a-4ca5-9652-a9b091c168be
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRdcFileWriter interface [Remote Differential Compression],Write method, IRdcFileWriter.Write, IRdcFileWriter::Write, Write, Write method [Remote Differential Compression], Write method [Remote Differential Compression],IRdcFileWriter interface, fs.irdcfilewriter_write, msrdc/IRdcFileWriter::Write, rdc.irdcfilewriter_write
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RdcMappingAccessMode
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a>
 

 

