---
UID: NF:imapi2fs.IFileSystemImage.LockInChangePoint
title: IFileSystemImage::LockInChangePoint (imapi2fs.h)
description: Locks the file system information at the current change-point level.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","LockInChangePoint method","IFileSystemImage.LockInChangePoint","IFileSystemImage::LockInChangePoint","LockInChangePoint","LockInChangePoint method [IMAPI]","LockInChangePoint method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_lockinchangepoint","imapi2fs/IFileSystemImage::LockInChangePoint"]
old-location: imapi\ifilesystemimage_lockinchangepoint.htm
tech.root: imapi
ms.assetid: ae5d659c-5da7-4478-b65f-64cbe227dbc5
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],LockInChangePoint method, IFileSystemImage.LockInChangePoint, IFileSystemImage::LockInChangePoint, LockInChangePoint, LockInChangePoint method [IMAPI], LockInChangePoint method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_lockinchangepoint, imapi2fs/IFileSystemImage::LockInChangePoint
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
 - IFileSystemImage::LockInChangePoint
 - imapi2fs/IFileSystemImage::LockInChangePoint
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
 - IFileSystemImage.LockInChangePoint
---

# IFileSystemImage::LockInChangePoint


## -description

Locks the file system information at the current change-point level.



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
<dt><b>IMAPI_E_FSI_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Internal error occurred: <i>%1!ls!</i>.

</td>
</tr>
</table>

## -remarks

Once the change point is locked, rollback to earlier change points is not permitted.

Locking the change point does not change the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_changepoint">IFileSystemImage::get_ChangePoint</a> property.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-rollbacktochangepoint">IFileSystemImage::RollbackToChangePoint</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_changepoint">IFileSystemImage::get_ChangePoint</a>
