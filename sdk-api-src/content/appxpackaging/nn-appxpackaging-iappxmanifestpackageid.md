---
UID: NN:appxpackaging.IAppxManifestPackageId
title: IAppxManifestPackageId
author: windows-sdk-content
description: Provides access to the package identity.
old-location: appxpkg\iappxmanifestpackageid.htm
old-project: appxpkg
ms.assetid: 8665AC2B-4D06-4684-99B1-E22533CA04AA
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxManifestPackageId, IAppxManifestPackageId interface [App packaging and management], IAppxManifestPackageId interface [App packaging and management],described, appxpackaging/IAppxManifestPackageId, appxpkg.iappxmanifestpackageid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestPackageId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageId interface


## -description


Provides access to the package identity.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageId</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxManifestPackageId</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageId</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8AC811D0-D5C5-47DF-92FD-C66BC018B668">ComparePublisher</a>
</td>
<td align="left" width="63%">
Compares the specified publisher with the publisher defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A332C96-9535-4BD3-B4D2-39559E430870">GetArchitecture</a>
</td>
<td align="left" width="63%">
Gets the processor architecture as defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F59FDC61-BA78-4204-AAD3-C34B7F1EB37B">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the package as defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4505020-61CB-4893-AB3B-6EF0E55FD225">GetPackageFamilyName</a>
</td>
<td align="left" width="63%">
Gets the package family name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/514D2E04-5CA5-4F45-A6D8-96866588EECF">GetPackageFullName</a>
</td>
<td align="left" width="63%">
Gets the package full name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C3B937D-5A70-480C-98F1-783D05D1810C">GetPublisher</a>
</td>
<td align="left" width="63%">
Gets the name of the package publisher as defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D17BD71A-6418-4229-8829-2C8EB9393285">GetResourceId</a>
</td>
<td align="left" width="63%">
Gets the package resource identifier as defined in the manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85684359-9244-4130-BF0F-56DDB6427345">GetVersion</a>
</td>
<td align="left" width="63%">
Gets the version of the package as defined in the manifest.

</td>
</tr>
</table> 


## -remarks



Package identity information is specified using the <a href="https://msdn.microsoft.com/45524773-3b61-44ac-a417-cfaac92af0a0">Identity</a> element in the package manifest.

This object can be retrieved using the <a href="https://msdn.microsoft.com/67E1B1A4-E934-4CCF-AF94-A7923B192A21">IAppxManifestReader::GetPackageId</a> method.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>



<a href="https://msdn.microsoft.com/67E1B1A4-E934-4CCF-AF94-A7923B192A21">IAppxManifestReader::GetPackageId</a>
 

 

