---
UID: NF:appxpackaging.IAppxManifestProperties.GetStringValue
title: IAppxManifestProperties::GetStringValue
author: windows-sdk-content
description: Gets the value of the specified string element in the properties section.
old-location: appxpkg\iappxmanifestproperties_getstringvalue.htm
tech.root: appxpkg
ms.assetid: 3EF2D8A2-37B2-4E57-9FD3-DA05FA90749C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStringValue, GetStringValue method [App packaging and management], GetStringValue method [App packaging and management],IAppxManifestProperties interface, IAppxManifestProperties interface [App packaging and management],GetStringValue method, IAppxManifestProperties.GetStringValue, IAppxManifestProperties::GetStringValue, appxpackaging/IAppxManifestProperties::GetStringValue, appxpkg.iappxmanifestproperties_getstringvalue
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
 - IAppxManifestProperties.GetStringValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestProperties::GetStringValue


## -description


Gets the value of the specified string element in the properties section.


## -parameters




### -param name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the string element. Valid values include:

<p class="indent">"Description"

<p class="indent">"DisplayName"

<p class="indent">"Logo"

<p class="indent">"PublisherDisplayName"


### -param value [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The value of the specified element.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If a valid string property with this name is not defined in the manifest, this method  returns <b>E_INVALIDARG</b> and  <i>value</i> receives a null string.

The caller must free the memory allocated for <i>value</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5DA0A805-13D3-4977-8EFB-45E8B51AAF60">IAppxManifestProperties</a>
 

 

