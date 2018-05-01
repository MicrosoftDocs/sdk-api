---
UID: NF:appxpackaging.IAppxBlockMapReader.GetStream
title: IAppxBlockMapReader::GetStream method
author: windows-driver-content
description: Retrieves a read-only stream that represents the XML content of the block map.
old-location: appxpkg\iappxblockmapreader_getstream.htm
old-project: appxpkg
ms.assetid: 95EBABDA-45D5-436C-B627-51C14D9091EA
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetStream method [App packaging and management], GetStream method [App packaging and management], IAppxBlockMapReader interface, GetStream,IAppxBlockMapReader.GetStream, IAppxBlockMapReader, IAppxBlockMapReader interface [App packaging and management], GetStream method, IAppxBlockMapReader::GetStream, appxpackaging/IAppxBlockMapReader::GetStream, appxpkg.iappxblockmapreader_getstream
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBlockMapReader.GetStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBlockMapReader::GetStream method


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
 

 

