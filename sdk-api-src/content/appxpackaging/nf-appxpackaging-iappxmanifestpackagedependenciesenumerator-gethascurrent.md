---
UID: NF:appxpackaging.IAppxManifestPackageDependenciesEnumerator.GetHasCurrent
title: IAppxManifestPackageDependenciesEnumerator::GetHasCurrent
author: windows-sdk-content
description: Determines whether there is a package dependency at the current position of the enumerator.
old-location: appxpkg\iappxmanifestpackagedependenciesenumerator_gethascurrent.htm
old-project: appxpkg
ms.assetid: 2D06DC83-B795-47F8-A05D-4DF4E86FEDFA
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxManifestPackageDependenciesEnumerator interface, IAppxManifestPackageDependenciesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxManifestPackageDependenciesEnumerator.GetHasCurrent, IAppxManifestPackageDependenciesEnumerator::GetHasCurrent, appxpackaging/IAppxManifestPackageDependenciesEnumerator::GetHasCurrent, appxpkg.iappxmanifestpackagedependenciesenumerator_gethascurrent
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
 - IAppxManifestPackageDependenciesEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageDependenciesEnumerator::GetHasCurrent


## -description


Determines whether there is a package dependency at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A09709AE-301F-4457-8E02-1A88FB283A43">IAppxManifestPackageDependenciesEnumerator</a>
 

 

