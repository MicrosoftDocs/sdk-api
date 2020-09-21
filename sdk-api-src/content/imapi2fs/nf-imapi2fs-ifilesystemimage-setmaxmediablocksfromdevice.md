---
UID: NF:imapi2fs.IFileSystemImage.SetMaxMediaBlocksFromDevice
title: IFileSystemImage::SetMaxMediaBlocksFromDevice (imapi2fs.h)
description: Set maximum number of blocks available based on the capabilities of the recorder.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","SetMaxMediaBlocksFromDevice method","IFileSystemImage.SetMaxMediaBlocksFromDevice","IFileSystemImage::SetMaxMediaBlocksFromDevice","SetMaxMediaBlocksFromDevice","SetMaxMediaBlocksFromDevice method [IMAPI]","SetMaxMediaBlocksFromDevice method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_setmaxmediablocksfromdevice","imapi2fs/IFileSystemImage::SetMaxMediaBlocksFromDevice"]
old-location: imapi\ifilesystemimage_setmaxmediablocksfromdevice.htm
tech.root: imapi
ms.assetid: 201e7390-68f3-48a4-9036-b07219fa3d80
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],SetMaxMediaBlocksFromDevice method, IFileSystemImage.SetMaxMediaBlocksFromDevice, IFileSystemImage::SetMaxMediaBlocksFromDevice, SetMaxMediaBlocksFromDevice, SetMaxMediaBlocksFromDevice method [IMAPI], SetMaxMediaBlocksFromDevice method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_setmaxmediablocksfromdevice, imapi2fs/IFileSystemImage::SetMaxMediaBlocksFromDevice
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
 - IFileSystemImage::SetMaxMediaBlocksFromDevice
 - imapi2fs/IFileSystemImage::SetMaxMediaBlocksFromDevice
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
 - IFileSystemImage.SetMaxMediaBlocksFromDevice
---

# IFileSystemImage::SetMaxMediaBlocksFromDevice


## -description

Set maximum number of blocks available based on the capabilities of the recorder.

## -parameters

### -param discRecorder [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface that identifies the recording device from which you want to set the maximum number of blocks available.

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

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>