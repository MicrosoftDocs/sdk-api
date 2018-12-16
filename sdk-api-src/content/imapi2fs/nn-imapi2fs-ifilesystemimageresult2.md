---
UID: NN:imapi2fs.IFileSystemImageResult2
title: IFileSystemImageResult2
author: windows-sdk-content
description: The IFileSystemImageResult2 interface allows the data recorder object to retrieve information about modified blocks in images created for rewritable discs.
old-location: imapi\ifilesystemimageresult2.htm
tech.root: imapi
ms.assetid: 83834da1-fa5a-42ef-8e59-7ba133d3e6cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFileSystemImageResult2, IFileSystemImageResult2 interface [IMAPI], IFileSystemImageResult2 interface [IMAPI],described, imapi.ifilesystemimageresult2, imapi2fs/IFileSystemImageResult2
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IFileSystemImageResult2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImageResult2 interface


## -description


The <b>IFileSystemImageResult2</b> interface allows the data recorder object to retrieve information about modified blocks in images created for rewritable discs. Alternatively, <b>IUnknown::QueryInterface</b> can be called on the object returned by <a href="https://msdn.microsoft.com/87e4bde6-c8c3-43b6-b096-514fdef5e262">IFileSystemImageResult::get_ImageStream</a> to get the <a href="https://msdn.microsoft.com/f2a3bd54-4f40-4bf0-9cbf-b507819d669f">IBlockRangeList</a> interface providing this information.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImageResult2</b> interface inherits from <a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>. <b>IFileSystemImageResult2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSystemImageResult2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2148ba3f-f334-43cb-965a-37b078419e0c">get_ModifiedBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the list of modified blocks in the result image.

</td>
</tr>
</table> 


## -remarks



When the file system image object is used to append data to a rewritable disc, the result image contains both the previous logical session and the new additions. The result image represents the binary data that must be recorded to disc starting from sector 0 to get a disc containing both old and new files. However, the previous logical session remains mostly intact during addition of new files, so the burn time can be substantially optimized by recording only the sectors that are new or have been modified.




## -see-also




<a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>
 

 

