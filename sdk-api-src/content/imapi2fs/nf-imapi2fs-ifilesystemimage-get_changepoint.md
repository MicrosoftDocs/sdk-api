---
UID: NF:imapi2fs.IFileSystemImage.get_ChangePoint
title: IFileSystemImage::get_ChangePoint (imapi2fs.h)
description: Retrieves the change point identifier.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_ChangePoint method","IFileSystemImage.get_ChangePoint","IFileSystemImage::get_ChangePoint","get_ChangePoint","get_ChangePoint method [IMAPI]","get_ChangePoint method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_changepoint","imapi2fs/IFileSystemImage::get_ChangePoint"]
old-location: imapi\ifilesystemimage_get_changepoint.htm
tech.root: imapi
ms.assetid: e5d15478-e632-4e76-91e2-ee360dfccf19
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_ChangePoint method, IFileSystemImage.get_ChangePoint, IFileSystemImage::get_ChangePoint, get_ChangePoint, get_ChangePoint method [IMAPI], get_ChangePoint method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_changepoint, imapi2fs/IFileSystemImage::get_ChangePoint
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
 - IFileSystemImage::get_ChangePoint
 - imapi2fs/IFileSystemImage::get_ChangePoint
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
 - IFileSystemImage.get_ChangePoint
---

# IFileSystemImage::get_ChangePoint


## -description

Retrieves the change point identifier.

## -parameters

### -param pVal [out]

Change point identifier. The identifier is a count of the changes to the file system image since its inception.

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

## -remarks

An application can store the value of this property prior to making a change to the file system, then at a later point pass the value to the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-rollbacktochangepoint">IFileSystemImage::RollbackToChangePoint</a> method to revert changes since that point in development.

An application can call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-lockinchangepoint">IFileSystemImage::LockInChangePoint</a> method to lock the state of  a file system image at any point in its development. Once a lock is set, you cannot call <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-rollbacktochangepoint">RollbackToChangePoint</a> to revert the file system image to its earlier state.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-lockinchangepoint">IFileSystemImage::LockInChangePoint</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-rollbacktochangepoint">IFileSystemImage::RollbackToChangePoint</a>