---
UID: NF:imapi2fs.IFileSystemImage.get_MultisessionInterfaces
title: IFileSystemImage::get_MultisessionInterfaces (imapi2fs.h)
description: Retrieves the list of multi-session interfaces for the optical media.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","get_MultisessionInterfaces method","IFileSystemImage.get_MultisessionInterfaces","IFileSystemImage::get_MultisessionInterfaces","get_MultisessionInterfaces","get_MultisessionInterfaces method [IMAPI]","get_MultisessionInterfaces method [IMAPI]","IFileSystemImage interface","imapi.ifilesystemimage_get_multisessioninterfaces","imapi2fs/IFileSystemImage::get_MultisessionInterfaces"]
old-location: imapi\ifilesystemimage_get_multisessioninterfaces.htm
tech.root: imapi
ms.assetid: 10c0b02e-965e-47ca-95f4-237c21b505ad
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],get_MultisessionInterfaces method, IFileSystemImage.get_MultisessionInterfaces, IFileSystemImage::get_MultisessionInterfaces, get_MultisessionInterfaces, get_MultisessionInterfaces method [IMAPI], get_MultisessionInterfaces method [IMAPI],IFileSystemImage interface, imapi.ifilesystemimage_get_multisessioninterfaces, imapi2fs/IFileSystemImage::get_MultisessionInterfaces
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
 - IFileSystemImage::get_MultisessionInterfaces
 - imapi2fs/IFileSystemImage::get_MultisessionInterfaces
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
 - IFileSystemImage.get_MultisessionInterfaces
---

# IFileSystemImage::get_MultisessionInterfaces


## -description

Retrieves the list of multi-session interfaces for the optical media.

## -parameters

### -param pVal [out]

List of multi-session interfaces for the optical media. Each element of the list is a <b>VARIANT</b> of type <b>VT_Dispatch</b>. Query the <b>pdispVal</b> member of the variant for the <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interface.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

Query the <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interface for a derived <b>IMultisession</b> interface, for example, the <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential">IMultisessionSequential</a> interface.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces">IFileSystemImage::put_MultisessionInterfaces</a>