---
UID: NF:appxpackaging.IAppxPackageReader.GetManifest
title: IAppxPackageReader::GetManifest
author: windows-sdk-content
description: Retrieves the object model of the app manifest of the package.
old-location: appxpkg\iappxpackagereader_getmanifest.htm
old-project: appxpkg
ms.assetid: 5EE69CCD-C941-4346-B539-C415CE9EA1FB
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: GetManifest, GetManifest method [App packaging and management], GetManifest method [App packaging and management],IAppxPackageReader interface, IAppxPackageReader interface [App packaging and management],GetManifest method, IAppxPackageReader.GetManifest, IAppxPackageReader::GetManifest, appxpackaging/IAppxPackageReader::GetManifest, appxpkg.iappxpackagereader_getmanifest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageReader.GetManifest
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageReader::GetManifest


## -description


Retrieves the object model of the app manifest of the package.


## -parameters




### -param manifestReader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>**</b>

The object model of the app manifest.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The package app manifest is validated when the package reader is created using <a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>
 

 

