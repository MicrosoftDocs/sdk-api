---
UID: NN:appxpackaging.IAppxFactory
title: IAppxFactory
author: windows-sdk-content
description: Creates objects for reading and writing app packages.
old-location: appxpkg\iappxfactory.htm
old-project: appxpkg
ms.assetid: 4EA79D44-7C26-4B65-81A1-394E1E540F34
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: IAppxFactory, IAppxFactory interface [App packaging and management], IAppxFactory interface [App packaging and management],described, appxpackaging/IAppxFactory, appxpkg.iappxfactory
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
 - IAppxFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxFactory interface


## -description


Creates objects for reading and writing app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B4A310F0-4276-49AA-9ABF-A98F41E8F87F">CreateBlockMapReader</a>
</td>
<td align="left" width="63%">
Creates a read-only block map object model from contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BF6C83FF-8CB1-47C0-84C3-E71059F0796E">CreateManifestReader</a>
</td>
<td align="left" width="63%">
Creates a read-only manifest object model from contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60C9781F-A1EE-4EAA-9CD5-32692F3E063D">CreatePackageReader</a>
</td>
<td align="left" width="63%">
Creates a read-only package reader from the contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>. This method does not validate the <a href="https://msdn.microsoft.com/DD88F9D9-E866-4941-8D04-B6959AC2F1CF">digital signature</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10E9250E-7A64-4FB0-ACB9-10CB144A0FBE">CreatePackageWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only package object to which  files can be added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCC39D9C-4AF9-4CFD-AC66-4B79F9F25BDC">CreateValidatedBlockMapReader</a>
</td>
<td align="left" width="63%">
Creates a read-only block map object model from contents provided by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> and a digital signature.

</td>
</tr>
</table> 


## -remarks



The <b>IAppxFactory</b> interface provides factory methods to create readers and writers of app packages as well as methods to create readers for block maps and manifests outside of a package.


#### Examples

For examples, see:

<ul>
<li>
<a href="https://msdn.microsoft.com/FD677D75-50D5-4228-891F-73B5F40679B0">How to create an app  package</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72C368F9-2EBA-4930-81CF-9B85717CC0AA">Quickstart: Extract app package contents</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A29986F9-C620-48CD-87F8-525DFA076AAB">Quickstart: Read app package manifest info</a>
</li>
</ul>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/233539FD-E3BE-4783-9F23-B34F6397FBBE">IAppxBlockMapReader</a>



<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>



<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>



<a href="https://msdn.microsoft.com/097B7451-9A54-4C39-8F83-16DB49691B42">IAppxPackageWriter</a>
 

 

