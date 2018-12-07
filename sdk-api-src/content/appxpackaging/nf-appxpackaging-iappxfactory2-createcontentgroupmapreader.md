---
UID: NF:appxpackaging.IAppxFactory2.CreateContentGroupMapReader
title: IAppxFactory2::CreateContentGroupMapReader
author: windows-sdk-content
description: Creates an IAppxContentGroupMapReader.
old-location: appxpkg\iappxfactory2_createcontentgroupmapreader.htm
tech.root: appxpkg
ms.assetid: 42453BD7-AB65-49E0-86C0-4F96B4234397
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateContentGroupMapReader, CreateContentGroupMapReader method [App packaging and management], CreateContentGroupMapReader method [App packaging and management],IAppxFactory2 interface, IAppxFactory2 interface [App packaging and management],CreateContentGroupMapReader method, IAppxFactory2.CreateContentGroupMapReader, IAppxFactory2::CreateContentGroupMapReader, appxpackaging/IAppxFactory2::CreateContentGroupMapReader, appxpkg.iappxfactory2_createcontentgroupmapreader
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
 - IAppxFactory2.CreateContentGroupMapReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxFactory2::CreateContentGroupMapReader


## -description


Creates an <a href="https://msdn.microsoft.com/45C6F61E-8CF6-4188-9715-3954562F8AB0">IAppxContentGroupMapReader</a>.


## -parameters




### -param inputStream [in]

The stream that delivers the content group map XML for reading.


### -param contentGroupMapReader [out, retval]

The content group map reader.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/01B11591-F854-4A39-8EDD-A5140235CA0B">IAppxFactory2</a>
 

 

