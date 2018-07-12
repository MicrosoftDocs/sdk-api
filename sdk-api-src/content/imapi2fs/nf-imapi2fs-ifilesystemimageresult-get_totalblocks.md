---
UID: NF:imapi2fs.IFileSystemImageResult.get_TotalBlocks
title: IFileSystemImageResult::get_TotalBlocks
author: windows-sdk-content
description: Retrieves the number of blocks in the result image.
old-location: imapi\ifilesystemimageresult_get_totalblocks.htm
old-project: imapi
ms.assetid: e895ed4f-67cb-43c2-aeb2-9a3ddb79c4fd
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_TotalBlocks method, IFileSystemImageResult.get_TotalBlocks, IFileSystemImageResult::get_TotalBlocks, get_TotalBlocks, get_TotalBlocks method [IMAPI], get_TotalBlocks method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_totalblocks, imapi2fs/IFileSystemImageResult::get_TotalBlocks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PlatformId
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImageResult.get_TotalBlocks
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IFileSystemImageResult::get_TotalBlocks


## -description


Retrieves the number of blocks in the result image.


## -parameters




### -param pVal [out]

Number of blocks to burn on the disc.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/30ec514c-97b8-41fc-b814-11f50cacaa25">IFileSystemImageResult</a>



<a href="https://msdn.microsoft.com/fe6d14d7-f3ae-4634-b8b4-1793f8007826">IFileSystemImageResult::get_BlockSize</a>
 

 

