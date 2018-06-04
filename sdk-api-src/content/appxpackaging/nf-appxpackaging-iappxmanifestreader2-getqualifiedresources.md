---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

