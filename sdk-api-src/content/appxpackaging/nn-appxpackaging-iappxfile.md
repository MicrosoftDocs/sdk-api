---
UID: NN:appxpackaging.IAppxFile
title: IAppxFile
author: windows-sdk-content
description: Retrieves information about a payload or footprint file in a package.
old-location: appxpkg\iappxfile.htm
tech.root: appxpkg
ms.assetid: DB09452D-725C-46EA-B74C-92C5E596BEF8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAppxFile, IAppxFile interface [App packaging and management], IAppxFile interface [App packaging and management],described, appxpackaging/IAppxFile, appxpkg.iappxfile
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
 - IAppxFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxFile interface


## -description


Retrieves information about a payload or footprint file in a package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxFile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2F33ED4-EAD3-44AE-B646-3AB875FA7606">GetCompressionOption</a>
</td>
<td align="left" width="63%">
Retrieves the compression option that is used to store the file in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86EE47E1-B2AD-4610-8C9A-679536F9C51D">GetContentType</a>
</td>
<td align="left" width="63%">
Retrieves the content type of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B56F7A31-686A-4A8B-9388-E30718632AE9">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file, including its path relative to the package root directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73353CE0-98F8-4A8C-A259-A07C125B9EE9">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the uncompressed size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B002A9A9-0BF5-4FB1-8D7D-06F7D066432C">GetStream</a>
</td>
<td align="left" width="63%">
Gets a read-only stream that contains the uncompressed content of the file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724">IAppxFilesEnumerator</a>
 

 

