---
UID: NN:shimgdata.IShellImageDataFactory
title: IShellImageDataFactory (shimgdata.h)
author: windows-sdk-content
description: Exposes methods that create IShellImageData instances based on various image sources.
old-location: shell\IShellImageDataFactory.htm
tech.root: shell
ms.assetid: c3de35de-9bf5-415c-93e9-ac0085195c27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellImageDataFactory, IShellImageDataFactory interface [Windows Shell], IShellImageDataFactory interface [Windows Shell],described, _shell_IShellImageDataFactory, shell.IShellImageDataFactory, shimgdata/IShellImageDataFactory
ms.topic: interface
f1_keywords: 
 - "shimgdata/IShellImageDataFactory"
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageDataFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellImageDataFactory interface


## -description


Exposes methods that create <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> instances based on various image sources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellImageDataFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellImageDataFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellImageDataFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedatafactory-createimagefromfile">CreateImageFromFile</a>
</td>
<td align="left" width="63%">
Creates an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> interface based on a given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedatafactory-createimagefromstream">CreateImageFromStream</a>
</td>
<td align="left" width="63%">
Creates an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> interface based on a given file stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedatafactory-createishellimagedata">CreateIShellImageData</a>
</td>
<td align="left" width="63%">
Creates an instance of the <a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedatafactory-getdataformatfrompath">GetDataFormatFromPath</a>
</td>
<td align="left" width="63%">
Determines a file's format based on its extension.

</td>
</tr>
</table> 


## -remarks



This interface is not expected to be available in later versions of Windows. It is recommended that Windows GDI+ APIs be used in place of <b>IShellImageDataFactory</b> methods.

This interface was not included in a public header file prior to Windows Vista.



