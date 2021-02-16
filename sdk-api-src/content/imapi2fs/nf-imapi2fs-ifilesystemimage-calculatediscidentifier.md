---
UID: NF:imapi2fs.IFileSystemImage.CalculateDiscIdentifier
title: IFileSystemImage::CalculateDiscIdentifier (imapi2fs.h)
description: Retrieves a string that identifies a disc and the sessions recorded on the disc.
helpviewer_keywords: ["CalculateDiscIdentifier","CalculateDiscIdentifier method [IMAPI]","CalculateDiscIdentifier method [IMAPI]","IFileSystemImage interface","IFileSystemImage interface [IMAPI]","CalculateDiscIdentifier method","IFileSystemImage.CalculateDiscIdentifier","IFileSystemImage::CalculateDiscIdentifier","imapi.ifilesystemimage_calculatediscidentifier","imapi2fs/IFileSystemImage::CalculateDiscIdentifier"]
old-location: imapi\ifilesystemimage_calculatediscidentifier.htm
tech.root: imapi
ms.assetid: c1d1fc83-326e-4d9f-b771-c520ee956ed5
ms.date: 12/05/2018
ms.keywords: CalculateDiscIdentifier, CalculateDiscIdentifier method [IMAPI], CalculateDiscIdentifier method [IMAPI],IFileSystemImage interface, IFileSystemImage interface [IMAPI],CalculateDiscIdentifier method, IFileSystemImage.CalculateDiscIdentifier, IFileSystemImage::CalculateDiscIdentifier, imapi.ifilesystemimage_calculatediscidentifier, imapi2fs/IFileSystemImage::CalculateDiscIdentifier
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
 - IFileSystemImage::CalculateDiscIdentifier
 - imapi2fs/IFileSystemImage::CalculateDiscIdentifier
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
 - IFileSystemImage.CalculateDiscIdentifier
---

# IFileSystemImage::CalculateDiscIdentifier


## -description

Retrieves a string that identifies a disc and the sessions recorded on the disc.

## -parameters

### -param discIdentifier [out]

String that contains a signature that identifies the disc and the sessions on it. This string is not guaranteed to be unique between discs.

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
<dt><b>IMAPI_E_MULTISESSION_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
MultisessionInterfaces property must be set prior calling this method.

Value: 0xC0AAB15D

</td>
</tr>
</table>

## -remarks

When layering sessions on a disc, the signature acts as a key that the client can use to ensure the session order, and to distinguish sessions on disc from session images that will be laid on the disc. 

You must call <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces">IFileSystemImage::put_MultisessionInterfaces</a> prior to calling <b>CalculateDiscIdentifier</b>.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>