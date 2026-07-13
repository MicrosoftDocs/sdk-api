---
UID: NF:appxpackaging.IAppxBlockMapFile.ValidateFileHash
title: IAppxBlockMapFile::ValidateFileHash (appxpackaging.h)
description: Validates the content of a file against the hashes stored in the block elements for this block map file.
helpviewer_keywords: ["IAppxBlockMapFile interface [App packaging and management]","ValidateFileHash method","IAppxBlockMapFile.ValidateFileHash","IAppxBlockMapFile::ValidateFileHash","ValidateFileHash","ValidateFileHash method [App packaging and management]","ValidateFileHash method [App packaging and management]","IAppxBlockMapFile interface","appxpackaging/IAppxBlockMapFile::ValidateFileHash","appxpkg.iappxblockmapfile_validatefilehash"]
old-location: appxpkg\iappxblockmapfile_validatefilehash.htm
tech.root: appxpkg
ms.assetid: 286EF8FD-925E-4B36-AFAB-D0EC949F8705
ms.date: 12/05/2018
ms.keywords: IAppxBlockMapFile interface [App packaging and management],ValidateFileHash method, IAppxBlockMapFile.ValidateFileHash, IAppxBlockMapFile::ValidateFileHash, ValidateFileHash, ValidateFileHash method [App packaging and management], ValidateFileHash method [App packaging and management],IAppxBlockMapFile interface, appxpackaging/IAppxBlockMapFile::ValidateFileHash, appxpkg.iappxblockmapfile_validatefilehash
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
 - IAppxBlockMapFile::ValidateFileHash
 - appxpackaging/IAppxBlockMapFile::ValidateFileHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBlockMapFile.ValidateFileHash
---

# IAppxBlockMapFile::ValidateFileHash


## -description

Validates the content of a file against the hashes stored in the block elements for this block map file.

## -parameters

### -param fileStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream that contains the file's contents. The stream must support <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>. If these methods fail, their error codes might be passed to and returned by this method.

### -param isValid [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the file hash validates; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfile">IAppxBlockMapFile</a>