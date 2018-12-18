---
UID: NF:appxpackaging.IAppxManifestApplication.GetStringValue
title: IAppxManifestApplication::GetStringValue
author: windows-sdk-content
description: Gets the value of a string element in the application metadata section of the manifest.
old-location: appxpkg\iappxmanifestapplication_getstringvalue.htm
tech.root: appxpkg
ms.assetid: 968EE95D-D1FC-42D7-B533-99062C26B4C3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStringValue, GetStringValue method [App packaging and management], GetStringValue method [App packaging and management],IAppxManifestApplication interface, IAppxManifestApplication interface [App packaging and management],GetStringValue method, IAppxManifestApplication.GetStringValue, IAppxManifestApplication::GetStringValue, appxpackaging/IAppxManifestApplication::GetStringValue, appxpkg.iappxmanifestapplication_getstringvalue
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
 - IAppxManifestApplication.GetStringValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestApplication::GetStringValue


## -description


Gets the value of a string element in the application metadata section of the manifest.


## -parameters




### -param name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

The name of the string element to get from the application metadata. Valid values include:

<p class="indent">"Description"

<p class="indent">"DisplayName"

<p class="indent">"EntryPoint"

<p class="indent">"Executable"

<p class="indent">"Id"

<p class="indent">"Logo"

<p class="indent">"SmallLogo"

<p class="indent">"StartPage"

<p class="indent">"Square150x150Logo" for Windows 8.1 and later

<p class="indent">"Square30x30Logo" for Windows 8.1 and later

<p class="indent">"BackgroundColor" for Windows 8.1 and later

<p class="indent">"ForegroundText" for Windows 8.1 and later

<p class="indent">"WideLogo" for Windows 8.1 and later

<p class="indent">"Wide310x310Logo" for Windows 8.1 and later

<p class="indent">"ShortName" for Windows 8.1 and later

<p class="indent">"Square310x310Logo" for Windows 8.1 and later

<p class="indent">"Square70x70Logo" for Windows 8.1 and later

<p class="indent">"MinWidth" for Windows 8.1 and later

Refer to the schema to determine where these values are being read from.


### -param value [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The value of the requested element.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the optional string value is not defined, this method returns <b>E_INVALIDARG</b> and <i>value</i> is <b>NULL</b>.

The caller must free the memory allocated for <i>value</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/16FC78D1-7387-4C90-9F63-BCFA110BC487">IAppxManifestApplication</a>
 

 

