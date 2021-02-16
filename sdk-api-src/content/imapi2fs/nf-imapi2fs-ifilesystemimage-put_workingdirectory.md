---
UID: NF:imapi2fs.IFileSystemImage.put_WorkingDirectory
title: IFileSystemImage::put_WorkingDirectory (imapi2fs.h)
description: Sets the temporary directory in which stash files are built.
helpviewer_keywords: ["IFileSystemImage interface [IMAPI]","put_WorkingDirectory method","IFileSystemImage.put_WorkingDirectory","IFileSystemImage::put_WorkingDirectory","imapi.ifilesystemimage_put_workingdirectory","imapi2fs/IFileSystemImage::put_WorkingDirectory","put_WorkingDirectory","put_WorkingDirectory method [IMAPI]","put_WorkingDirectory method [IMAPI]","IFileSystemImage interface"]
old-location: imapi\ifilesystemimage_put_workingdirectory.htm
tech.root: imapi
ms.assetid: bfe37cfe-654d-4923-b667-e44be7ce4715
ms.date: 12/05/2018
ms.keywords: IFileSystemImage interface [IMAPI],put_WorkingDirectory method, IFileSystemImage.put_WorkingDirectory, IFileSystemImage::put_WorkingDirectory, imapi.ifilesystemimage_put_workingdirectory, imapi2fs/IFileSystemImage::put_WorkingDirectory, put_WorkingDirectory, put_WorkingDirectory method [IMAPI], put_WorkingDirectory method [IMAPI],IFileSystemImage interface
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
 - IFileSystemImage::put_WorkingDirectory
 - imapi2fs/IFileSystemImage::put_WorkingDirectory
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
 - IFileSystemImage.put_WorkingDirectory
---

# IFileSystemImage::put_WorkingDirectory


## -description

Sets the temporary directory in which stash files are built.

## -parameters

### -param newVal [in]

String that contains the path to the temporary working directory. The default is the current temp directory.

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
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The value specified for parameter <i>%1!ls!</i> is not valid.

Value: 0xC0AAB101

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_WORKING_DIRECTORY</b></dt>
</dl>
</td>
<td width="60%">
The working directory <i>%1!ls!</i> is not valid.

Value: 0xC0AAB140

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_WORKING_DIRECTORY_SPACE</b></dt>
</dl>
</td>
<td width="60%">
Cannot set working directory to <i>%1!ls!</i>. Space available is <i>%2!I64d!</i> bytes, approximately <i>%3!I64d!</i> bytes required. 

Value: 0xC0AAB141

</td>
</tr>
</table>

## -remarks

  
Stash files are the temporary files used to build the file-system image.

An exception results if the existing stash files cannot move to the new working directory. 

You cannot change the working directory if a result stream exists for the file-system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_workingdirectory">IFileSystemImage::get_WorkingDirectory</a>