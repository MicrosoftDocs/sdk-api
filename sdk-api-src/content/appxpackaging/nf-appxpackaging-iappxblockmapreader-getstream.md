---
UID: NF:appxpackaging.IAppxBlockMapReader.GetStream
title: IAppxBlockMapReader::GetStream
author: windows-sdk-content
description: Retrieves a read-only stream that represents the XML content of the block map.
old-location: appxpkg\iappxblockmapreader_getstream.htm
tech.root: appxpkg
ms.assetid: 95EBABDA-45D5-436C-B627-51C14D9091EA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStream, GetStream method [App packaging and management], GetStream method [App packaging and management],IAppxBlockMapReader interface, IAppxBlockMapReader interface [App packaging and management],GetStream method, IAppxBlockMapReader.GetStream, IAppxBlockMapReader::GetStream, appxpackaging/IAppxBlockMapReader::GetStream, appxpkg.iappxblockmapreader_getstream
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBlockMapReader.GetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBlockMapReader::GetStream


## -description


Retrieves a read-only stream that represents the XML content of the block map.


## -parameters




### -param blockMapStream [out, retval]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

A read-only stream that represents the XML content of the block map.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>
 

 

