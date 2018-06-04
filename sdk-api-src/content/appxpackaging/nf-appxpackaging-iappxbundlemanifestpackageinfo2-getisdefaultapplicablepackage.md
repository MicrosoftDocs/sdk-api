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

# IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage


## -description


Determines whether the app package is a default applicable package.


## -parameters




### -param isDefaultApplicablePackage [out, retval]

True if the package is a default applicable package, False otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A default applicable package is a package that contains the default MRT-qualified resources. For example, a default applicable package could be English language resources that should be installed by default if no other appropriate alternative language is  available.

For more information on app resources, see <a href="https://docs.microsoft.com/windows/uwp/app-resources/">App resources and the Resource Management System</a>.




## -see-also




<a href="https://msdn.microsoft.com/036CD1E1-F4D7-46B9-A287-2728BA45348A">IAppxBundleManifestPackageInfo2</a>
 

 

