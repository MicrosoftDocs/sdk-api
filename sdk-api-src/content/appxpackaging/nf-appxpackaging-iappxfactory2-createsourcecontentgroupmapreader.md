---
UID: NF:appxpackaging.IAppxFactory2.CreateSourceContentGroupMapReader
title: IAppxFactory2::CreateSourceContentGroupMapReader
author: windows-sdk-content
description: Creates an IAppxSourceContentGroupMapReader.
old-location: appxpkg\iappxfactory2_createsourcecontentgroupmapreader.htm
tech.root: appxpkg
ms.assetid: DB0FFB8D-A9DB-4B9C-B277-76623ECA3D6B
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CreateSourceContentGroupMapReader, CreateSourceContentGroupMapReader method [App packaging and management], CreateSourceContentGroupMapReader method [App packaging and management],IAppxFactory2 interface, IAppxFactory2 interface [App packaging and management],CreateSourceContentGroupMapReader method, IAppxFactory2.CreateSourceContentGroupMapReader, IAppxFactory2::CreateSourceContentGroupMapReader, appxpackaging/IAppxFactory2::CreateSourceContentGroupMapReader, appxpkg.iappxfactory2_createsourcecontentgroupmapreader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IAppxFactory2.CreateSourceContentGroupMapReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxFactory2::CreateSourceContentGroupMapReader


## -description


Creates an <a href="https://msdn.microsoft.com/EA0DF7E6-C4EF-4A58-A13F-EB3789239084">IAppxSourceContentGroupMapReader</a>.


## -parameters




### -param inputStream [in]

The stream that delivers the source content group map XML for reading.


### -param reader [out, retval]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/01B11591-F854-4A39-8EDD-A5140235CA0B">IAppxFactory2</a>
 

 

