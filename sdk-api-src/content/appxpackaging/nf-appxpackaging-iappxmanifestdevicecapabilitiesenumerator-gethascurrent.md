---
UID: NF:appxpackaging.IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent
title: IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a device capability at the current position of the enumerator.
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxManifestDeviceCapabilitiesEnumerator interface","IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent","IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent","appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent","appxpkg.iappxmanifestdevicecapabilitiesenumerator_gethascurrent"]
old-location: appxpkg\iappxmanifestdevicecapabilitiesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: 52E0C961-F947-4F66-B3A0-21AB0F64C4B4
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxManifestDeviceCapabilitiesEnumerator interface, IAppxManifestDeviceCapabilitiesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent, IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent, appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent, appxpkg.iappxmanifestdevicecapabilitiesenumerator_gethascurrent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent
 - appxpackaging/IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestDeviceCapabilitiesEnumerator.GetHasCurrent
---

# IAppxManifestDeviceCapabilitiesEnumerator::GetHasCurrent


## -description

Determines whether there is a device capability at the current position of the enumerator.

## -parameters

### -param hasCurrent [retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestdevicecapabilitiesenumerator">IAppxManifestDeviceCapabilitiesEnumerator</a>