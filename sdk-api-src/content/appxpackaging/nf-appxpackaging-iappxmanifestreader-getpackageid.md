---
UID: NF:appxpackaging.IAppxManifestReader.GetPackageId
title: IAppxManifestReader::GetPackageId
author: windows-driver-content
description: Gets the package identifier defined in the manifest.
old-location: appxpkg\iappxmanifestreader_getpackageid.htm
old-project: appxpkg
ms.assetid: 67E1B1A4-E934-4CCF-AF94-A7923B192A21
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetPackageId, GetPackageId method [App packaging and management], GetPackageId method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetPackageId method, IAppxManifestReader.GetPackageId, IAppxManifestReader::GetPackageId, appxpackaging/IAppxManifestReader::GetPackageId, appxpkg.iappxmanifestreader_getpackageid
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
-	IAppxManifestReader.GetPackageId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader::GetPackageId


## -description


Gets the package identifier defined in the manifest.


## -parameters




### -param packageId [out, retval]

Type: <b><a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>**</b>

The package identifier.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <i>packageId</i> object.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

