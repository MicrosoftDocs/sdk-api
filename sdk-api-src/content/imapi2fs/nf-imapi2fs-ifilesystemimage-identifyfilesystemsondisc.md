---
UID: NF:imapi2fs.IFileSystemImage.IdentifyFileSystemsOnDisc
title: IFileSystemImage::IdentifyFileSystemsOnDisc (imapi2fs.h)
description: Retrieves a list of the different types of file systems on the optical media.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","IdentifyFileSystemsOnDisc method","IFileSystemImage.IdentifyFileSystemsOnDisc","IFileSystemImage::IdentifyFileSystemsOnDisc","IdentifyFileSystemsOnDisc","IdentifyFileSystemsOnDisc method [IMAPI]","IdentifyFileSystemsOnDisc method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_identifyfilesystemsondisc","imapi2fs/IFileSystemImage::IdentifyFileSystemsOnDisc"]
old-location: imapi\ifilesystemimage_identifyfilesystemsondisc.htm
tech.root: imapi
ms.assetid: 381be283-c877-44f0-9d96-b9e80a6aeec8
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],IdentifyFileSystemsOnDisc method, IFileSystemImage.IdentifyFileSystemsOnDisc, IFileSystemImage::IdentifyFileSystemsOnDisc, IdentifyFileSystemsOnDisc, IdentifyFileSystemsOnDisc method [IMAPI], IdentifyFileSystemsOnDisc method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_identifyfilesystemsondisc, imapi2fs/IFileSystemImage::IdentifyFileSystemsOnDisc
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
 - IFileSystemImage::IdentifyFileSystemsOnDisc
 - imapi2fs/IFileSystemImage::IdentifyFileSystemsOnDisc
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
 - IFileSystemImage.IdentifyFileSystemsOnDisc
---

# IFileSystemImage::IdentifyFileSystemsOnDisc


## -description

Retrieves a list of the different types of file systems on the optical media.

## -parameters

### -param discRecorder [in, optional]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface that identifies the recording device that contains the media. If this parameter is <b>NULL</b>, the <i>discRecorder</i>  specified in <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> will be used.

### -param fileSystems [out]

One or more files systems on the disc. For possible values, see <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a> enumeration type.

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

Client applications can call <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-getdefaultfilesystemforimport">IFileSystemImage::GetDefaultFileSystemForImport</a> with the value returned by this method to determine the type of file system to import.

## -see-also

<a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>