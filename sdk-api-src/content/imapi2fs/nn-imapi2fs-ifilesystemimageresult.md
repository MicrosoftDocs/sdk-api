---
UID: NN:imapi2fs.IFileSystemImageResult
title: IFileSystemImageResult (imapi2fs.h)
author: windows-sdk-content
description: Use this interface to get information about the burn image, the image data stream, and progress information.
old-location: imapi\ifilesystemimageresult.htm
tech.root: imapi
ms.assetid: 30ec514c-97b8-41fc-b814-11f50cacaa25
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult, IFileSystemImageResult interface [IMAPI], IFileSystemImageResult interface [IMAPI],described, imapi.ifilesystemimageresult, imapi2fs/IFileSystemImageResult
ms.topic: interface
f1_keywords: ["imapi2fs/IFileSystemImageResult"]
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IFileSystemImageResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSystemImageResult interface


## -description


Use this interface to get information about the burn image, the image data stream, and progress information.

To get this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">IFileSystemImage::CreateResultImage</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImageResult</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFileSystemImageResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemImageResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_blocksize">get_BlockSize</a>
</td>
<td align="left" width="63%">
Retrieves the size, in bytes, of a block of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_discid">get_DiscId</a>
</td>
<td align="left" width="63%">
Retrieves the disc volume name for this file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_imagestream">get_ImageStream</a>
</td>
<td align="left" width="63%">
Retrieves the burn image stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_progressitems">get_ProgressItems</a>
</td>
<td align="left" width="63%">
Retrieves the progress item block mapping collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_totalblocks">get_TotalBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the number of blocks in the result image.

</td>
</tr>
</table> 


## -remarks



This is an <b>FileSystemImageResult</b> object in script.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">IFileSystemImage::CreateResultImage</a>
 

 

