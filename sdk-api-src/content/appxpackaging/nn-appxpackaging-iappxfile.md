---
UID: NN:appxpackaging.IAppxFile
title: IAppxFile (appxpackaging.h)
description: Retrieves information about a payload or footprint file in a package.
helpviewer_keywords: ["IAppxFile","IAppxFile interface [App packaging and management]","IAppxFile interface [App packaging and management]","described","appxpackaging/IAppxFile","appxpkg.iappxfile"]
old-location: appxpkg\iappxfile.htm
tech.root: appxpkg
ms.assetid: DB09452D-725C-46EA-B74C-92C5E596BEF8
ms.date: 12/05/2018
ms.keywords: IAppxFile, IAppxFile interface [App packaging and management], IAppxFile interface [App packaging and management],described, appxpackaging/IAppxFile, appxpkg.iappxfile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFile
 - appxpackaging/IAppxFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFile
---

# IAppxFile interface


## -description

Retrieves information about a payload or footprint file in a package.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxFile</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfile-getcompressionoption">GetCompressionOption</a>
</td>
<td align="left" width="63%">
Retrieves the compression option that is used to store the file in the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfile-getcontenttype">GetContentType</a>
</td>
<td align="left" width="63%">
Retrieves the content type of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfile-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the file, including its path relative to the package root directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfile-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the uncompressed size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfile-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Gets a read-only stream that contains the uncompressed content of the file.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfilesenumerator">IAppxFilesEnumerator</a>

