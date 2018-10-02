---
UID: NF:appxpackaging.IAppxManifestReader.GetPackageDependencies
title: IAppxManifestReader::GetPackageDependencies
author: windows-sdk-content
description: Gets an enumerator that iterates through dependencies defined in the manifest.
old-location: appxpkg\iappxmanifestreader_getpackagedependencies.htm
tech.root: appxpkg
ms.assetid: C40276CC-8F97-4DCF-A5C4-193453B8FA02
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetPackageDependencies, GetPackageDependencies method [App packaging and management], GetPackageDependencies method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetPackageDependencies method, IAppxManifestReader.GetPackageDependencies, IAppxManifestReader::GetPackageDependencies, appxpackaging/IAppxManifestReader::GetPackageDependencies, appxpkg.iappxmanifestreader_getpackagedependencies
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
 - IAppxManifestReader.GetPackageDependencies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestReader::GetPackageDependencies


## -description


Gets an enumerator that iterates through dependencies defined in the manifest. 


## -parameters




### -param dependencies [out, retval]

Type: <b><a href="https://msdn.microsoft.com/A09709AE-301F-4457-8E02-1A88FB283A43">IAppxManifestPackageDependenciesEnumerator</a>**</b>

The enumerator that iterates through the dependencies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no package dependencies are found in the manifest, this method returns <b>S_OK</b> with an  empty enumerator.

Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <i>dependencies</i> object.




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

