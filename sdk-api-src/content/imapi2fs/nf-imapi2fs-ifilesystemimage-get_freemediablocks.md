---
UID: NF:imapi2fs.IFileSystemImage.get_FreeMediaBlocks
title: IFileSystemImage::get_FreeMediaBlocks
author: windows-sdk-content
description: Retrieves the maximum number of blocks available for the image.
old-location: imapi\ifilesystemimage_get_freemediablocks.htm
tech.root: imapi
ms.assetid: 4942d86d-0cc7-4f4e-b257-dc59d3896b38
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_FreeMediaBlocks method, IFileSystemImage.get_FreeMediaBlocks, IFileSystemImage::get_FreeMediaBlocks, get_FreeMediaBlocks, get_FreeMediaBlocks method [IMAPI], get_FreeMediaBlocks method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_freemediablocks, imapi2fs/IFileSystemImage::get_FreeMediaBlocks
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFileSystemImage.get_FreeMediaBlocks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2fs.h
: 
- IFileSystemImage.get_FreeMediaBlocks
: 
---

# IFileSystemImage::get_FreeMediaBlocks


## -description


Retrieves the maximum number of blocks available for the image.


## -parameters




### -param pVal [out]

Number of blocks to use in creating the file system image. 


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




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/7ffa2736-6480-4bda-8144-b949bf43e580">IFileSystemImage::put_FreeMediaBlocks</a>



<a href="https://msdn.microsoft.com/9211b8af-9331-4d0d-a6f5-f52f8db42e8c">IFilesystemImage::ChooseImageDefaults</a>



<a href="https://msdn.microsoft.com/1d327da0-d0b3-4fcf-9773-ff5ea1eeea1c">IFilesystemImage::ChooseImageDefaultsForMediaType</a>
 

 

