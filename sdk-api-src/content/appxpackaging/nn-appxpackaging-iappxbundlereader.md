---
UID: NN:appxpackaging.IAppxBundleReader
title: IAppxBundleReader
author: windows-sdk-content
description: Provides a read-only object model for bundle packages.
old-location: appxpkg\iappxbundlereader.htm
tech.root: appxpkg
ms.assetid: 3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAppxBundleReader, IAppxBundleReader interface [App packaging and management], IAppxBundleReader interface [App packaging and management],described, appxpackaging/IAppxBundleReader, appxpkg.iappxbundlereader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleReader interface


## -description


Provides a read-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/721940C7-0680-4AD0-93BC-20D630EDE228">GetBlockMap</a>
</td>
<td align="left" width="63%">
Retrieves a read-only block map object from the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD60CD3E-2C08-4B97-B311-00C0EEBEF752">GetFootprintFile</a>
</td>
<td align="left" width="63%">
Retrieves the specified type of footprint file from the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C9D80910-8609-45D9-A3EC-05A033A36A4F">GetManifest</a>
</td>
<td align="left" width="63%">
Retrieves a read-only manifest object from the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ACAB26C-22FC-45D7-9F6A-98B56B615DCA">GetPayloadPackage</a>
</td>
<td align="left" width="63%">
Retrieves an appx file object for the payload package with the specified file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90C1CF98-D33F-4643-8978-7C74A4E5BD52">GetPayloadPackages</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that iterates over the list of all payload packages in the bundle. 

</td>
</tr>
</table> 


## -remarks



You can use the <a href="https://msdn.microsoft.com/3D9F7A0A-EF6A-4C99-B9A0-C618138DB5ED">CreateBundleReader</a> method of the <a href="https://msdn.microsoft.com/33A320BD-7B68-4C42-A776-25CC744C6652">IAppxBundleFactory</a> interface to retrieve the <b>IAppxBundleReader</b> object. 

Through <b>IAppxBundleReader</b>, you can retrieve both footprint files, such as the bundle’s manifest, block map, and signature, and app packages that are contained in the bundle.



