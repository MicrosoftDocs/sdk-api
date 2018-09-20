---
UID: NN:imapi2fs.IProgressItem
title: IProgressItem
author: windows-sdk-content
description: Use this interface to retrieve block information for one segment of the result file image.
old-location: imapi\iprogressitem.htm
tech.root: imapi
ms.assetid: b6ba9226-655e-4eac-ad43-2b5a8e90039f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IProgressItem, IProgressItem interface [IMAPI], IProgressItem interface [IMAPI],described, imapi.iprogressitem, imapi2fs/IProgressItem
ms.prod: windows
ms.technology: windows-sdk
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressItem interface


## -description


Use this interface to retrieve block information for one segment of the result file image. This can be used to determine the LBA ranges of files in the resulting image. This information can then be used to display to the user which file is currently being written to the media or used for other advanced burning functionality.

To get this interface, call the <a href="https://msdn.microsoft.com/9a6b4838-921b-444d-8ac2-f26d9762d9ce">IEnumProgressItems::Next</a> or <a href="https://msdn.microsoft.com/c5f85ca3-1bad-49fd-9e67-d41135cd837d">IEnumProgressItems::RemoteNext</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProgressItem</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IProgressItem</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6960fecb-f202-4a10-9abb-fc945217a314">get_BlockCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of blocks in the progress item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72da165f-a875-4f26-a2ba-701ad0a4a9d1">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the description in the progress item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c1c5932-0301-4752-871d-609d3c128906">get_FirstBlock</a>
</td>
<td align="left" width="63%">
Retrieves the first block number in this segment of the result image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad75e708-4a10-45b9-89c2-11270f6edd9e">get_LastBlock</a>
</td>
<td align="left" width="63%">
Retrieves the last block in this segment of the result image.

</td>
</tr>
</table> 


## -remarks



This is a <b>ProgressItem</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/c4238fbe-762a-492f-9eb5-d927e64436e1">IEnumProgressItems</a>



<a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>



<a href="https://msdn.microsoft.com/40c28e67-8ff3-4330-90a1-7ebccb0023ad">IProgressItems</a>
 

 

