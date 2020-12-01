---
UID: NF:imapi2fs.IFsiItem.FileSystemPath
title: IFsiItem::FileSystemPath (imapi2fs.h)
description: Retrieves the full path of the item as modified to conform to the specified file system.
helpviewer_keywords: ["FileSystemPath","FileSystemPath method [IMAPI]","FileSystemPath method [IMAPI]","IFsiItem interface","IFsiItem interface [IMAPI]","FileSystemPath method","IFsiItem.FileSystemPath","IFsiItem::FileSystemPath","imapi.ifsiitem_filesystempath","imapi2fs/IFsiItem::FileSystemPath"]
old-location: imapi\ifsiitem_filesystempath.htm
tech.root: imapi
ms.assetid: c6b969e2-9b1c-402e-81ea-ced13fca4551
ms.date: 12/05/2018
ms.keywords: FileSystemPath, FileSystemPath method [IMAPI], FileSystemPath method [IMAPI],IFsiItem interface, IFsiItem interface [IMAPI],FileSystemPath method, IFsiItem.FileSystemPath, IFsiItem::FileSystemPath, imapi.ifsiitem_filesystempath, imapi2fs/IFsiItem::FileSystemPath
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
 - IFsiItem::FileSystemPath
 - imapi2fs/IFsiItem::FileSystemPath
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
 - IFsiItem.FileSystemPath
---

# IFsiItem::FileSystemPath


## -description

Retrieves the full path of the item as modified to conform to the specified file system.

## -parameters

### -param fileSystem [in]

File system to which the path should conform. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-fsifilesystems">FsiFileSystems</a> enumeration type.

### -param pVal [out]

String that contains the full path of the item as it conforms to the specified file system. The path in the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_fullpath">IFsiItem::get_FullPath</a> property is modified if the characters used and its length do not meet the requirements of the specified file system type.

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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>