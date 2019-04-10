---
UID: NF:appxpackaging.IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent
title: IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent (appxpackaging.h)
author: windows-sdk-content
description: Determines whether there is a device capability at the current position of the enumerator.
old-location: appxpkg\iappxmanifestdevicecapabilitiesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: 52E0C961-F947-4F66-B3A0-21AB0F64C4B4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxManifestDeviceCapabilitiesEnumerator interface, IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent, IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent, appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent, appxpkg.iappxmanifestdevicecapabilitiesenumerator_gethascurrent
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
 - IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent


## -description


Determines whether there is a device capability at the current position of the enumerator.


## -parameters




### -param hasCurrent [retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6A544E15-BB92-48C3-963D-789B04464277">IAppxManifestDeviceCapabilitiesEnumerator</a>
 

 

