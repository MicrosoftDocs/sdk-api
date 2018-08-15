---
UID: NF:msrdc.IRdcLibrary.CreateSignatureReader
title: IRdcLibrary::CreateSignatureReader
author: windows-sdk-content
description: Creates a signature reader to allow an application to decode the contents of a signature file.
old-location: rdc\irdclibrary_createsignaturereader.htm
old-project: Rdc
ms.assetid: 08627c9d-7470-47ab-9209-32734082c393
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CreateSignatureReader, CreateSignatureReader method [Remote Differential Compression], CreateSignatureReader method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],CreateSignatureReader method, IRdcLibrary.CreateSignatureReader, IRdcLibrary::CreateSignatureReader, fs.irdclibrary_createsignaturereader, msrdc/IRdcLibrary::CreateSignatureReader, rdc.irdclibrary_createsignaturereader
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
 - IRdcLibrary.CreateSignatureReader
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRdcLibrary::CreateSignatureReader


## -description


The <b>CreateSignatureReader</b> method 
    creates a signature reader to allow an application to decode the contents of a signature 
    file.


## -parameters




### -param iFileReader [in]

An <a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a> interface pointer initialized to read the signatures.


### -param iSignatureReader [out]

Pointer to a location that will receive an 
    <a href="https://msdn.microsoft.com/dec6eb10-1243-4888-9ccc-ab1f4cfb11e7">IRdcSignatureReader</a> interface pointer. On a 
  successful return the interface will be initialized on return. Callers must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9684efca-37fd-45ce-a24e-d5276b8ea6af">IRdcFileReader</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>



<a href="https://msdn.microsoft.com/dec6eb10-1243-4888-9ccc-ab1f4cfb11e7">IRdcSignatureReader</a>
 

 

