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
 

 

