---
UID: NF:appxpackaging.IAppxManifestReader2.GetQualifiedResources
title: IAppxManifestReader2::GetQualifiedResources (appxpackaging.h)
author: windows-sdk-content
description: Gets an enumerator that iterates through the qualified resources that are defined in the manifest.
old-location: appxpkg\iappxmanifestreader2_getqualifiedresources.htm
tech.root: appxpkg
ms.assetid: C712DA82-CA4F-4C5B-A391-3B40D5EE61C4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetQualifiedResources, GetQualifiedResources method [App packaging and management], GetQualifiedResources method [App packaging and management],IAppxManifestReader2 interface, IAppxManifestReader2 interface [App packaging and management],GetQualifiedResources method, IAppxManifestReader2.GetQualifiedResources, IAppxManifestReader2::GetQualifiedResources, appxpackaging/IAppxManifestReader2::GetQualifiedResources, appxpkg.iappxmanifestreader2_getqualifiedresources
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
 - IAppxManifestReader2.GetQualifiedResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestReader2::GetQualifiedResources


## -description


Gets an enumerator that iterates through the qualified resources that are defined in the manifest.


## -parameters




### -param resources [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9F58B665-3C3D-407C-B872-FC915CE97B0E">IAppxManifestQualifiedResourcesEnumerator</a>**</b>

The enumerator that iterates through the qualified resources.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



Resources are specified using the <a href="https://msdn.microsoft.com/45ce3dac-3888-452b-bc10-8775b158637a">Resources</a> element in the manifest.

Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <i>resources</i> object.




## -see-also




<a href="https://msdn.microsoft.com/B10A1ACB-12F4-4338-A6D6-6D2B829F9D62">IAppxManifestReader2</a>
 

 

