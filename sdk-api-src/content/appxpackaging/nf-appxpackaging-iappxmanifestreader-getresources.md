---
UID: NF:appxpackaging.IAppxManifestReader.GetResources
title: IAppxManifestReader::GetResources
author: windows-driver-content
description: Gets an enumerator that iterates through the resources defined in the manifest.
old-location: appxpkg\iappxmanifestreader_getresources.htm
old-project: appxpkg
ms.assetid: 2F0109C2-99F5-4AEE-9596-153764FA8FA3
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetResources, GetResources method [App packaging and management], GetResources method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetResources method, IAppxManifestReader.GetResources, IAppxManifestReader::GetResources, appxpackaging/IAppxManifestReader::GetResources, appxpkg.iappxmanifestreader_getresources
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
-	IAppxManifestReader.GetResources
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader::GetResources


## -description


Gets an enumerator that iterates through the resources defined in the manifest.


## -parameters




### -param resources [out, retval]

Type: <b><a href="https://msdn.microsoft.com/D76C7512-962F-4AFE-934F-BBC215B5FE99">IAppxManifestResourcesEnumerator</a>**</b>

The enumerator that iterates through the resources.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



Resources are specified using the <a href="https://msdn.microsoft.com/45ce3dac-3888-452b-bc10-8775b158637a">Resources</a> element in the manifest.

Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <i>resources</i> object.




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

