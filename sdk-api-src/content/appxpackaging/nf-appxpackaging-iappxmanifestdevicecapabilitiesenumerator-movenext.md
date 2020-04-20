---
UID: NF:appxpackaging.IAppxManifestDeviceCapabilitiesEnumerator.MoveNext
title: IAppxManifestDeviceCapabilitiesEnumerator::MoveNext (appxpackaging.h)
description: Advances the position of the enumerator to the next device capability.helpviewer_keywords: ["IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management]","MoveNext method","IAppxManifestDeviceCapabilitiesEnumerator.MoveNext","IAppxManifestDeviceCapabilitiesEnumerator::MoveNext","MoveNext","MoveNext method [App packaging and management]","MoveNext method [App packaging and management]","IAppxManifestDeviceCapabilitiesEnumerator interface","appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::MoveNext","appxpkg.iappxmanifestdevicecapabilitiesenumerator_movenext"]
old-location: appxpkg\iappxmanifestdevicecapabilitiesenumerator_movenext.htm
tech.root: appxpkg
ms.assetid: 2FD0F98C-2B20-47B2-8F86-F59E3E9B9086
ms.date: 12/05/2018
ms.keywords: IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management],MoveNext method, IAppxManifestDeviceCapabilitiesEnumerator.MoveNext, IAppxManifestDeviceCapabilitiesEnumerator::MoveNext, MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management],IAppxManifestDeviceCapabilitiesEnumerator interface, appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::MoveNext, appxpkg.iappxmanifestdevicecapabilitiesenumerator_movenext
f1_keywords:
- appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator.MoveNext
dev_langs:
- c++
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
- IAppxManifestDeviceCapabilitiesEnumerator.MoveNext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestDeviceCapabilitiesEnumerator::MoveNext


## -description


Advances the position of the enumerator to the next device capability.


## -parameters




### -param hasNext [retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

Note that when the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another MoveNext after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestdevicecapabilitiesenumerator">IAppxManifestDeviceCapabilitiesEnumerator</a>
 

 

