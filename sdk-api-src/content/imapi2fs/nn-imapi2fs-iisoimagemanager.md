---
UID: NN:imapi2fs.IIsoImageManager
title: IIsoImageManager (imapi2fs.h)
author: windows-sdk-content
description: Use this interface to verify if an existing .iso file contains a valid file system for burning.
old-location: imapi\iisoimagemanager.htm
tech.root: imapi
ms.assetid: 47b059a9-a18a-4f32-9a02-6566175ca86b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIsoImageManager, IIsoImageManager interface [IMAPI], IIsoImageManager interface [IMAPI],described, imapi.iisoimagemanager, imapi2fs/IIsoImageManager
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2fs.h
api_name:
 - IIsoImageManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsoImageManager interface


## -description


Use this interface to verify if an existing .iso file contains a valid file system for burning.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsoImageManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IIsoImageManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsoImageManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56166789-8eeb-4468-a85e-b35e665170d6">get_Path</a>
</td>
<td align="left" width="63%">
Retrieves the logical path to an .iso image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0655edb2-5dce-4428-b883-984ef53712cd">get_Stream</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IStream</b> object associated with the .iso image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e5ef908-795d-4617-8123-605855b9ddc8">SetPath</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/56166789-8eeb-4468-a85e-b35e665170d6">Path</a> property with a logical path to an .iso image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ee540aa-8ccc-40cb-afc8-b1790cabee6e">SetStream</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/0655edb2-5dce-4428-b883-984ef53712cd">Stream</a> property with an <b>IStream</b> object associated with the .iso image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fd9f0fc-8a77-4b94-9111-c8ce223329b6">Validate</a>
</td>
<td align="left" width="63%">
Determines if the provided .iso image is valid.

</td>
</tr>
</table> 


## -remarks



If a valid path is provided via <a href="https://msdn.microsoft.com/3e5ef908-795d-4617-8123-605855b9ddc8">SetPath</a>, an <b>IStream</b> object will be created from the supplied image file and the <b>Stream</b> property will be populated.
If a valid <b>IStream</b> is provided via <a href="https://msdn.microsoft.com/3ee540aa-8ccc-40cb-afc8-b1790cabee6e">SetStream</a>, it will be used directly for image validation and the <b>Path</b> property will not be populated.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.



