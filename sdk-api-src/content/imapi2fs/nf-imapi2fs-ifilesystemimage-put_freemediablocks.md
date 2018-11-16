---
UID: NF:imapi2fs.IFileSystemImage.put_FreeMediaBlocks
title: IFileSystemImage::put_FreeMediaBlocks
author: windows-sdk-content
description: Sets the maximum number of blocks available for the image.
old-location: imapi\ifilesystemimage_put_freemediablocks.htm
tech.root: imapi
ms.assetid: 7ffa2736-6480-4bda-8144-b949bf43e580
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_FreeMediaBlocks method, IFileSystemImage.put_FreeMediaBlocks, IFileSystemImage::put_FreeMediaBlocks, imapi.ifilesystemimage_put_freemediablocks, imapi2fs/IFileSystemImage::put_FreeMediaBlocks, put_FreeMediaBlocks, put_FreeMediaBlocks method [IMAPI], put_FreeMediaBlocks method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage.put_FreeMediaBlocks
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
- IFileSystemImage.put_FreeMediaBlocks
: 
---

# IFileSystemImage::put_FreeMediaBlocks


## -description


Sets the maximum number of blocks available for the image.


## -parameters




### -param newVal [in]

Number of blocks to use in creating the file system image. 

By default, 332,800 blocks are used to create the file system image. This value assumes a capacity of 74 minutes of audio per 650MB disc.

To specify an infinite number of block, set <i>newVal</i> to zero.


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
<dt><b>IMAPI_E_IMAGE_TOO_BIG</b></dt>
</dl>
</td>
<td width="60%">
Value specified for FreeMediaBlocks property is too small for estimated image size based on current data. 

Value: 0xC0AAB121

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/4942d86d-0cc7-4f4e-b257-dc59d3896b38">IFileSystemImage::get_FreeMediaBlocks</a>
 

 

