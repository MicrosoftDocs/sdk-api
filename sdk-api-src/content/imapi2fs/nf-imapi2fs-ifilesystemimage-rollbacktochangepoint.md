---
UID: NF:imapi2fs.IFileSystemImage.RollbackToChangePoint
title: IFileSystemImage::RollbackToChangePoint (imapi2fs.h)
description: Reverts the image back to the specified change point.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","RollbackToChangePoint method","IFileSystemImage.RollbackToChangePoint","IFileSystemImage::RollbackToChangePoint","RollbackToChangePoint","RollbackToChangePoint method [IMAPI]","RollbackToChangePoint method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_rollbacktochangepoint","imapi2fs/IFileSystemImage::RollbackToChangePoint"]
old-location: imapi\ifilesystemimage_rollbacktochangepoint.htm
tech.root: imapi
ms.assetid: 852b88ed-6af7-4fe6-bf5f-831d55423130
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],RollbackToChangePoint method, IFileSystemImage.RollbackToChangePoint, IFileSystemImage::RollbackToChangePoint, RollbackToChangePoint, RollbackToChangePoint method [IMAPI], RollbackToChangePoint method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_rollbacktochangepoint, imapi2fs/IFileSystemImage::RollbackToChangePoint
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
 - IFileSystemImage::RollbackToChangePoint
 - imapi2fs/IFileSystemImage::RollbackToChangePoint
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
 - IFileSystemImage.RollbackToChangePoint
---

# IFileSystemImage::RollbackToChangePoint


## -description

Reverts the image back to the specified change point.

## -parameters

### -param changePoint [in]

Change point that identifies the target state for rollback.

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
<dt><b>IMAPI_E_TOO_MANY_DIRS</b></dt>
</dl>
</td>
<td width="60%">
This file system image has too many directories for the <i>%1!ls!</i> file system.

Value: 0xC0AAB130

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_ISO9660_LEVELS</b></dt>
</dl>
</td>
<td width="60%">
ISO9660 is limited to 8 levels of directories.

Value: 0xC0AAB131

</td>
</tr>
</table>

## -remarks

Typically, an application calls the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_changepoint">IFileSystemImage::get_ChangePoint</a> method and stores the change point value prior to making a change to the file system. If necessary, you can pass the change point value to this method to revert changes since that point in development.

An application can call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-lockinchangepoint">IFileSystemImage::LockInChangePoint</a> method to lock the state of  a file system image at any point in its development. After a lock is set, you cannot call this method to revert the file system image to its earlier state.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-lockinchangepoint">IFileSystemImage::LockInChangePoint</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_changepoint">IFileSystemImage::get_ChangePoint</a>