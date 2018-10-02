---
UID: NF:appxpackaging.IAppxBundleReader.GetManifest
title: IAppxBundleReader::GetManifest
author: windows-sdk-content
description: Retrieves a read-only manifest object from the bundle.
old-location: appxpkg\iappxbundlereader_getmanifest.htm
tech.root: appxpkg
ms.assetid: C9D80910-8609-45D9-A3EC-05A033A36A4F
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetManifest, GetManifest method [App packaging and management], GetManifest method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetManifest method, IAppxBundleReader.GetManifest, IAppxBundleReader::GetManifest, appxpackaging/IAppxBundleReader::GetManifest, appxpkg.iappxbundlereader_getmanifest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleReader.GetManifest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleReader::GetManifest


## -description


Retrieves a read-only manifest object from the bundle.


## -parameters




### -param manifestReader [out, retval]

Type: <b>IAppxBundleManifestReader**</b>

The object model of the bundle manifest.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664">IAppxBundleReader</a>
 

 

