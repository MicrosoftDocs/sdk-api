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

# IAppxManifestPackageDependency2::GetMaxMajorVersionTested


## -description


Returns the maximum major version number of  the package that is tested to be compatible
with the current package.


## -parameters




### -param maxMajorVersionTested [out]

The maximum major version number of the dependency package that has been tested to be compatible
with the current package.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If the
<b>MaxMajorVersionTested</b> attribute is not specified for the current dependency package, this method returns the highest 16 bits of the <b>MinVersion</b> field. For more information, see the <a href="https://msdn.microsoft.com/301053BA-A2DB-405C-9E2E-3817B2B5D7FD">GetMinVersion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/301053BA-A2DB-405C-9E2E-3817B2B5D7FD">GetMinVersion</a>



<a href="https://msdn.microsoft.com/9363C5BB-BDEF-4671-9545-5B8C0EF14FBE">IAppxManifestPackageDependency2</a>
 

 

