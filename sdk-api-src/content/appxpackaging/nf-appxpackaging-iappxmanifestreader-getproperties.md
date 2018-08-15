---
UID: NF:appxpackaging.IAppxManifestReader.GetProperties
title: IAppxManifestReader::GetProperties
author: windows-sdk-content
description: Gets the properties of the package as defined in the manifest.
old-location: appxpkg\iappxmanifestreader_getproperties.htm
old-project: appxpkg
ms.assetid: E507BA9D-D2CA-4B28-BD13-B820B666B4C6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetProperties, GetProperties method [App packaging and management], GetProperties method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetProperties method, IAppxManifestReader.GetProperties, IAppxManifestReader::GetProperties, appxpackaging/IAppxManifestReader::GetProperties, appxpkg.iappxmanifestreader_getproperties
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
 - IAppxManifestReader.GetProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader::GetProperties


## -description


Gets the properties of the package as defined in the manifest. 


## -parameters




### -param packageProperties [out, retval]

Type: <b><a href="https://msdn.microsoft.com/5DA0A805-13D3-4977-8EFB-45E8B51AAF60">IAppxManifestProperties</a>**</b>

Properties of the package as described by the manifest.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



Properties are specified using the <a href="https://msdn.microsoft.com/0847bddc-08ad-4f0b-b1ef-9987916e9c98">Properties</a> element in the manifest.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

