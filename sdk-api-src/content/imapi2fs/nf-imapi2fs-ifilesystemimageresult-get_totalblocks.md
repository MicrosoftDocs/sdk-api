---
UID: NF:imapi2fs.IFileSystemImageResult.get_TotalBlocks
title: IFileSystemImageResult::get_TotalBlocks (imapi2fs.h)
author: windows-sdk-content
description: Retrieves the number of blocks in the result image.
old-location: imapi\ifilesystemimageresult_get_totalblocks.htm
tech.root: imapi
ms.assetid: e895ed4f-67cb-43c2-aeb2-9a3ddb79c4fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSystemImageResult interface [IMAPI],get_TotalBlocks method, IFileSystemImageResult.get_TotalBlocks, IFileSystemImageResult::get_TotalBlocks, get_TotalBlocks, get_TotalBlocks method [IMAPI], get_TotalBlocks method [IMAPI],IFileSystemImageResult interface, imapi.ifilesystemimageresult_get_totalblocks, imapi2fs/IFileSystemImageResult::get_TotalBlocks
ms.topic: method
f1_keywords: 
 - "imapi2fs/IFileSystemImageResult.get_TotalBlocks"
dev_langs:
 - c++
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
 - IFileSystemImageResult.get_TotalBlocks
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult">IFileSystemImageResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimageresult-get_blocksize">IFileSystemImageResult::get_BlockSize</a>
 

 

