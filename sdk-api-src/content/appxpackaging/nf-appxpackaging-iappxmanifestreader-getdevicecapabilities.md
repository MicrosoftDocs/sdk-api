---
UID: NF:appxpackaging.IAppxManifestReader.GetDeviceCapabilities
title: IAppxManifestReader::GetDeviceCapabilities
author: windows-sdk-content
description: Gets an enumerator that iterates through the device capabilities defined in the manifest.
old-location: appxpkg\iappxmanifestreader_getdevicecapabilities.htm
old-project: appxpkg
ms.assetid: 06257DB1-992E-4A8D-8221-76DA3DF0FA1F
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetDeviceCapabilities, GetDeviceCapabilities method [App packaging and management], GetDeviceCapabilities method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetDeviceCapabilities method, IAppxManifestReader.GetDeviceCapabilities, IAppxManifestReader::GetDeviceCapabilities, appxpackaging/IAppxManifestReader::GetDeviceCapabilities, appxpkg.iappxmanifestreader_getdevicecapabilities
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestReader.GetDeviceCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestReader::GetDeviceCapabilities


## -description


Gets an enumerator that iterates through the device capabilities defined in the manifest.


## -parameters




### -param deviceCapabilities [out, retval]

Type: <b><a href="https://msdn.microsoft.com/6A544E15-BB92-48C3-963D-789B04464277">IAppxManifestDeviceCapabilitiesEnumerator</a>**</b>

The enumerator that iterates through the device capabilities.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Device capabilities are specified using the <a href="https://msdn.microsoft.com/4353c4fd-f038-4986-81ed-d2ec0c6235ef">DeviceCapability</a> element in the package manifest.

If no package device capabilities are defined in the manifest, this method returns <b>S_OK</b> with an  empty enumerator.

Call the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when you have finished using the <i>deviceCapabilities</i> object.




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

