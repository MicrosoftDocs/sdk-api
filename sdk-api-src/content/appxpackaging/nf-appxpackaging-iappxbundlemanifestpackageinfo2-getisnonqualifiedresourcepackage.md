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

# IAppxBundleManifestPackageInfo2::GetIsNonQualifiedResourcePackage


## -description


Determines whether the app package is a non-qualified resource package.


## -parameters




### -param isNonQualifiedResourcePackage [out, retval]

True if the package is a non-qualified resource package, False otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A non-qualified resource package is a package that contains resources that are not qualified with any language, scale, or other qualifier. An example of this could be a package that contains all music files. 

For more information on app resources, see <a href="https://docs.microsoft.com/windows/uwp/app-resources/">App resources and the Resource Management System</a>.




## -see-also




<a href="https://msdn.microsoft.com/036CD1E1-F4D7-46B9-A287-2728BA45348A">IAppxBundleManifestPackageInfo2</a>
 

 

