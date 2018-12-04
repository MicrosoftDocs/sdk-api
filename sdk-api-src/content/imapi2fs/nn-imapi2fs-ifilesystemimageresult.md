---
UID: NN:imapi2fs.IFileSystemImageResult
title: IFileSystemImageResult
author: windows-sdk-content
description: Use this interface to get information about the burn image, the image data stream, and progress information.
old-location: imapi\ifilesystemimageresult.htm
tech.root: imapi
ms.assetid: 30ec514c-97b8-41fc-b814-11f50cacaa25
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFileSystemImageResult, IFileSystemImageResult interface [IMAPI], IFileSystemImageResult interface [IMAPI],described, imapi.ifilesystemimageresult, imapi2fs/IFileSystemImageResult
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFileSystemImageResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileSystemImageResult interface


## -description


Use this interface to get information about the burn image, the image data stream, and progress information.

To get this interface, call the <a href="https://msdn.microsoft.com/6f7d2438-5c80-4461-8b48-646f0ca44498">IFileSystemImage::CreateResultImage</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSystemImageResult</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFileSystemImageResult</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fe6d14d7-f3ae-4634-b8b4-1793f8007826">get_BlockSize</a>
</td>
<td align="left" width="63%">
Retrieves the size, in bytes, of a block of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2288b4e4-6f36-4830-a077-dcf710741911">get_DiscId</a>
</td>
<td align="left" width="63%">
Retrieves the disc volume name for this file system image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87e4bde6-c8c3-43b6-b096-514fdef5e262">get_ImageStream</a>
</td>
<td align="left" width="63%">
Retrieves the burn image stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4ef572d-7e18-4537-847c-419441befe00">get_ProgressItems</a>
</td>
<td align="left" width="63%">
Retrieves the progress item block mapping collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e895ed4f-67cb-43c2-aeb2-9a3ddb79c4fd">get_TotalBlocks</a>
</td>
<td align="left" width="63%">
Retrieves the number of blocks in the result image.

</td>
</tr>
</table> 


## -remarks



This is an <b>FileSystemImageResult</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>



<a href="https://msdn.microsoft.com/6f7d2438-5c80-4461-8b48-646f0ca44498">IFileSystemImage::CreateResultImage</a>
 

 

