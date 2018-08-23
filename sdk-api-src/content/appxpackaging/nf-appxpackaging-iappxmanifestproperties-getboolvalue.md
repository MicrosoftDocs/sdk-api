---
UID: NF:appxpackaging.IAppxManifestProperties.GetBoolValue
title: IAppxManifestProperties::GetBoolValue
author: windows-sdk-content
description: Gets the value of the specified Boolean element in the properties section.
old-location: appxpkg\iappxmanifestproperties_getboolvalue.htm
old-project: appxpkg
ms.assetid: 228FD28A-E65E-484B-81EF-83CC993F05D6
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: GetBoolValue, GetBoolValue method [App packaging and management], GetBoolValue method [App packaging and management],IAppxManifestProperties interface, IAppxManifestProperties interface [App packaging and management],GetBoolValue method, IAppxManifestProperties.GetBoolValue, IAppxManifestProperties::GetBoolValue, appxpackaging/IAppxManifestProperties::GetBoolValue, appxpkg.iappxmanifestproperties_getboolvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.redist: 
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
 - IAppxManifestProperties.GetBoolValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestProperties::GetBoolValue


## -description


Gets the value of the specified Boolean element in the properties section.


## -parameters




### -param name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the Boolean element. Valid values include:

<p class="indent">"Framework"

<p class="indent">"ResourcePackage" for Windows 8.1 and later


### -param value [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

The value of the specified Boolean element.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If a valid Boolean property with this name is not defined in the manifest, this method  returns <b>E_INVALIDARG</b> and <i>value</i> is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/5DA0A805-13D3-4977-8EFB-45E8B51AAF60">IAppxManifestProperties</a>
 

 

