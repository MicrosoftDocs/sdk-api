---
UID: NN:imapi2fs.IProgressItem
title: IProgressItem (imapi2fs.h)
author: windows-sdk-content
description: Use this interface to retrieve block information for one segment of the result file image.
old-location: imapi\iprogressitem.htm
tech.root: imapi
ms.assetid: b6ba9226-655e-4eac-ad43-2b5a8e90039f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProgressItem, IProgressItem interface [IMAPI], IProgressItem interface [IMAPI],described, imapi.iprogressitem, imapi2fs/IProgressItem
ms.topic: interface
f1_keywords: 
 - "imapi2fs/IProgressItem"
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
 - IProgressItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProgressItem interface


## -description


Use this interface to retrieve block information for one segment of the result file image. This can be used to determine the LBA ranges of files in the resulting image. This information can then be used to display to the user which file is currently being written to the media or used for other advanced burning functionality.

To get this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next">IEnumProgressItems::Next</a> or <a href="https://docs.microsoft.com/windows/desktop/imapi/ienumprogressitems-remotenext">IEnumProgressItems::RemoteNext</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProgressItem</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IProgressItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProgressItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitem-get_blockcount">get_BlockCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of blocks in the progress item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitem-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the description in the progress item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitem-get_firstblock">get_FirstBlock</a>
</td>
<td align="left" width="63%">
Retrieves the first block number in this segment of the result image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-iprogressitem-get_lastblock">get_LastBlock</a>
</td>
<td align="left" width="63%">
Retrieves the last block in this segment of the result image.

</td>
</tr>
</table> 


## -remarks



This is a <b>ProgressItem</b> object in script.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems">IEnumProgressItems</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>
 

 

