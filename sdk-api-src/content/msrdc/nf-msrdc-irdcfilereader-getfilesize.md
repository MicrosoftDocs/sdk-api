---
UID: NF:msrdc.IRdcFileReader.GetFileSize
title: IRdcFileReader::GetFileSize (msrdc.h)
author: windows-sdk-content
description: Returns the size of a file.
old-location: rdc\irdcfilereader_getfilesize.htm
tech.root: rdc
ms.assetid: 2db66eb0-7213-446a-ad4b-f0df9e48abd4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFileSize, GetFileSize method [Remote Differential Compression], GetFileSize method [Remote Differential Compression],IRdcFileReader interface, IRdcFileReader interface [Remote Differential Compression],GetFileSize method, IRdcFileReader.GetFileSize, IRdcFileReader::GetFileSize, fs.irdcfilereader_getfilesize, msrdc/IRdcFileReader::GetFileSize, rdc.irdcfilereader_getfilesize
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
req.type-library: MsRdc.dll
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
 - IRdcFileReader.GetFileSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>
 

 

