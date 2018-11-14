---
UID: NF:appxpackaging.IAppxBundleReader.GetPayloadPackages
title: IAppxBundleReader::GetPayloadPackages
author: windows-sdk-content
description: Retrieves an enumerator that iterates over the list of all payload packages in the bundle.
old-location: appxpkg\iappxbundlereader_getpayloadpackages.htm
tech.root: appxpkg
ms.assetid: 90C1CF98-D33F-4643-8978-7C74A4E5BD52
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetPayloadPackages, GetPayloadPackages method [App packaging and management], GetPayloadPackages method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetPayloadPackages method, IAppxBundleReader.GetPayloadPackages, IAppxBundleReader::GetPayloadPackages, appxpackaging/IAppxBundleReader::GetPayloadPackages, appxpkg.iappxbundlereader_getpayloadpackages
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
 - IAppxBundleReader.GetPayloadPackages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- appxpackaging.h
: 
- IAppxBundleReader.GetPayloadPackages
: 
---

# IAppxBundleReader::GetPayloadPackages


## -description


Retrieves an enumerator that iterates over the list of all payload packages in the bundle. 


## -parameters




### -param payloadPackages [out, retval]

Type: <b><a href="https://msdn.microsoft.com/A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724">IAppxFilesEnumerator</a>**</b>

 An enumerator over all payload packages in the bundle. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664">IAppxBundleReader</a>
 

 

