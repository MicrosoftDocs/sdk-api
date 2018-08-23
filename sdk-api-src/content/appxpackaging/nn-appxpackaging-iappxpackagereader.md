---
UID: NN:appxpackaging.IAppxPackageReader
title: IAppxPackageReader
author: windows-sdk-content
description: Provides a read-only object model for app packages.
old-location: appxpkg\iappxpackagereader.htm
old-project: appxpkg
ms.assetid: D34D0909-BE2B-4182-8C3D-36A4E8DDC820
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: IAppxPackageReader, IAppxPackageReader interface [App packaging and management], IAppxPackageReader interface [App packaging and management],described, appxpackaging/IAppxPackageReader, appxpkg.iappxpackagereader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IAppxPackageReader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageReader interface


## -description


Provides a read-only object model for app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxPackageReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxPackageReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxPackageReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FEBCA2E4-9B32-499B-AD31-9D90525A42DB">GetBlockMap</a>
</td>
<td align="left" width="63%">
Retrieves the block map object model of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8CCF9135-308F-4BDC-A67F-1E3ED2ACF565">GetFootprintFile</a>
</td>
<td align="left" width="63%">
Retrieves a footprint file from the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5EE69CCD-C941-4346-B539-C415CE9EA1FB">GetManifest</a>
</td>
<td align="left" width="63%">
Retrieves the object model of the app manifest of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83E6931D-405C-4A93-BE70-F505D484CB7F">GetPayloadFile</a>
</td>
<td align="left" width="63%">
Retrieves a payload file from the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20883A4E-BE7B-4312-978A-3BF9362CA6DA">GetPayloadFiles</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that iterates through the payload files in the package.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxPackageReader</b> interface provides the ability to access payload files from a package and to query metadata from footprint files. 

This object can be retrieved using the <a href="https://msdn.microsoft.com/60C9781F-A1EE-4EAA-9CD5-32692F3E063D">CreatePackageReader</a> method of the <a href="https://msdn.microsoft.com/4EA79D44-7C26-4B65-81A1-394E1E540F34">IAppxFactory</a> interface.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/72C368F9-2EBA-4930-81CF-9B85717CC0AA">Quickstart: Extract app package contents</a> and <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/097B7451-9A54-4C39-8F83-16DB49691B42">IAppxPackageWriter</a>
 

 

