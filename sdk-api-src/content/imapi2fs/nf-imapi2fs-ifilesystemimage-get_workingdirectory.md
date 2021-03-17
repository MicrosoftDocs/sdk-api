---
UID: NF:imapi2fs.IFileSystemImage.get_WorkingDirectory
title: IFileSystemImage::get_WorkingDirectory (imapi2fs.h)
description: Retrieves the temporary directory in which stash files are built.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_WorkingDirectory method","IFileSystemImage.get_WorkingDirectory","IFileSystemImage::get_WorkingDirectory","get_WorkingDirectory","get_WorkingDirectory method [IMAPI]","get_WorkingDirectory method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_workingdirectory","imapi2fs/IFileSystemImage::get_WorkingDirectory"]
old-location: imapi\ifilesystemimage_get_workingdirectory.htm
tech.root: imapi
ms.assetid: 89c4fd34-6651-4056-9939-201f404ea6ee
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_WorkingDirectory method, IFileSystemImage.get_WorkingDirectory, IFileSystemImage::get_WorkingDirectory, get_WorkingDirectory, get_WorkingDirectory method [IMAPI], get_WorkingDirectory method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_workingdirectory, imapi2fs/IFileSystemImage::get_WorkingDirectory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileSystemImage::get_WorkingDirectory
 - imapi2fs/IFileSystemImage::get_WorkingDirectory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IFileSystemImage.get_WorkingDirectory
---

# IFileSystemImage::get_WorkingDirectory


## -description

Retrieves the temporary directory in which stash files are built.

## -parameters

### -param pVal [out]

String that contains the path to the temporary directory.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_workingdirectory">IFileSystemImage::put_WorkingDirectory</a>