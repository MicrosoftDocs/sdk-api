---
UID: NF:appxpackaging.IAppxManifestResourcesEnumerator.GetHasCurrent
title: IAppxManifestResourcesEnumerator::GetHasCurrent
author: windows-sdk-content
description: Determines whether there is a resource at the current position of the enumerator.
old-location: appxpkg\iappxmanifestresourcesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: 72798FDF-3296-4AC7-9BA0-212457F9BEC7
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxManifestResourcesEnumerator interface, IAppxManifestResourcesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxManifestResourcesEnumerator.GetHasCurrent, IAppxManifestResourcesEnumerator::GetHasCurrent, appxpackaging/IAppxManifestResourcesEnumerator::GetHasCurrent, appxpkg.iappxmanifestresourcesenumerator_gethascurrent
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
 - IAppxManifestResourcesEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestResourcesEnumerator::GetHasCurrent


## -description


Determines whether there is a resource at the current position of the enumerator.


## -parameters




### -param hasCurrent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D76C7512-962F-4AFE-934F-BBC215B5FE99">IAppxManifestResourcesEnumerator</a>
 

 

