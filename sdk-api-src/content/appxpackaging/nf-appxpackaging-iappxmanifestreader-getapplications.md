---
UID: NF:appxpackaging.IAppxManifestReader.GetApplications
title: IAppxManifestReader::GetApplications
author: windows-sdk-content
description: Gets an enumerator that iterates through the applications defined in the manifest.
old-location: appxpkg\iappxmanifestreader_getapplications.htm
old-project: appxpkg
ms.assetid: EC575692-93D6-43F1-857B-9A27DD50B8FC
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: GetApplications, GetApplications method [App packaging and management], GetApplications method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetApplications method, IAppxManifestReader.GetApplications, IAppxManifestReader::GetApplications, appxpackaging/IAppxManifestReader::GetApplications, appxpkg.iappxmanifestreader_getapplications
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxManifestReader.GetApplications
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader::GetApplications


## -description


Gets an enumerator that iterates through the applications defined in the manifest.


## -parameters




### -param applications [out, retval]

Type: <b><a href="https://msdn.microsoft.com/49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F">IAppxManifestApplicationsEnumerator</a>**</b>

The enumerator that iterates through the applications.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no applications are defined in the manifest, this method returns <b>S_OK</b> with an  empty <a href="https://msdn.microsoft.com/49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F">IAppxManifestApplicationsEnumerator</a> object.

Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a> object.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

