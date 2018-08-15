---
UID: NF:msrdc.IRdcFileReader.Read
title: IRdcFileReader::Read
author: windows-sdk-content
description: Reads the specified amount of data starting at the specified position.
old-location: rdc\irdcfilereader_read.htm
old-project: Rdc
ms.assetid: 194944c8-94a8-4f9b-9970-012392e069b1
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IRdcFileReader interface [Remote Differential Compression],Read method, IRdcFileReader.Read, IRdcFileReader::Read, Read, Read method [Remote Differential Compression], Read method [Remote Differential Compression],IRdcFileReader interface, fs.irdcfilereader_read, msrdc/IRdcFileReader::Read, rdc.irdcfilereader_read
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
req.type-library: MsRdc.dll
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
 - IRdcFileReader.Read
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Typically RDC will read the file sequentially from start to end. When reading signatures, the file may be read 
    more than once.

If the <b>BOOL</b> pointed to by the <i>eof</i> parameter is not <b>TRUE</b> 
    on return then the value pointed to by the <i>bytesActuallyRead</i> parameter must equal the 
    <i>bytesToRead</i> parameter. If the value pointed to by the <i>eof</i> 
    parameter is set, then the value pointed to by the <i>bytesActuallyRead</i> parameter can be 
    any value between zero and the <i>bytesToRead</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>
 

 

