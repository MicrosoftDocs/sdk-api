---
UID: NN:dwrite.IDWriteFontFileStream
title: IDWriteFontFileStream
author: windows-sdk-content
description: Loads font file data from a custom font file loader.
old-location: directwrite\IDWriteFontFileStream.htm
tech.root: DirectWrite
ms.assetid: 792ab9be-853f-427d-a762-2da8e81423f8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDWriteFontFileStream, IDWriteFontFileStream interface [Direct Write], IDWriteFontFileStream interface [Direct Write],described, directwrite.IDWriteFontFileStream, dwrite/IDWriteFontFileStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFileStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFileStream interface


## -description


 Loads font file data from a custom font file loader. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFileStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFileStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFileStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52186ddb-ea08-4615-a3df-35ea7288270c">GetFileSize</a>
</td>
<td align="left" width="63%">
 Obtains the total size of a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb4045c0-a333-40aa-8ec3-b89cfd835be3">GetLastWriteTime</a>
</td>
<td align="left" width="63%">
 Obtains the last modified time of the file. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5bf3300-cfa0-43db-b513-6c0d695c564e">ReadFileFragment</a>
</td>
<td align="left" width="63%">
 Reads a fragment from a font file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a12c28e-5595-4255-8fdd-5d546ceed90b">ReleaseFileFragment</a>
</td>
<td align="left" width="63%">
 Releases a fragment from a file.

</td>
</tr>
</table> 

