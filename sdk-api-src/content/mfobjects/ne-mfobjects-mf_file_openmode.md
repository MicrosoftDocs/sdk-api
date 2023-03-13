---
UID: NE:mfobjects.__MIDL___MIDL_itf_mfobjects_0000_0017_0002
title: MF_FILE_OPENMODE (mfobjects.h)
description: Specifies how to open or create a file.
helpviewer_keywords: ["0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6","MF_FILE_OPENMODE","MF_FILE_OPENMODE enumeration [Media Foundation]","MF_OPENMODE_APPEND_IF_EXIST","MF_OPENMODE_DELETE_IF_EXIST","MF_OPENMODE_FAIL_IF_EXIST","MF_OPENMODE_FAIL_IF_NOT_EXIST","MF_OPENMODE_RESET_IF_EXIST","__MIDL___MIDL_itf_mfobjects_0000_0017_0002","mf.mf_file_openmode","mfobjects/MF_FILE_OPENMODE","mfobjects/MF_OPENMODE_APPEND_IF_EXIST","mfobjects/MF_OPENMODE_DELETE_IF_EXIST","mfobjects/MF_OPENMODE_FAIL_IF_EXIST","mfobjects/MF_OPENMODE_FAIL_IF_NOT_EXIST","mfobjects/MF_OPENMODE_RESET_IF_EXIST"]
old-location: mf\mf_file_openmode.htm
tech.root: mf
ms.assetid: 0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6
ms.date: 12/05/2018
ms.keywords: 0c0e94fa-cbcc-4abc-9020-af6d36a4d3b6, MF_FILE_OPENMODE, MF_FILE_OPENMODE enumeration [Media Foundation], MF_OPENMODE_APPEND_IF_EXIST, MF_OPENMODE_DELETE_IF_EXIST, MF_OPENMODE_FAIL_IF_EXIST, MF_OPENMODE_FAIL_IF_NOT_EXIST, MF_OPENMODE_RESET_IF_EXIST, __MIDL___MIDL_itf_mfobjects_0000_0017_0002, mf.mf_file_openmode, mfobjects/MF_FILE_OPENMODE, mfobjects/MF_OPENMODE_APPEND_IF_EXIST, mfobjects/MF_OPENMODE_DELETE_IF_EXIST, mfobjects/MF_OPENMODE_FAIL_IF_EXIST, mfobjects/MF_OPENMODE_FAIL_IF_NOT_EXIST, mfobjects/MF_OPENMODE_RESET_IF_EXIST
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MF_FILE_OPENMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mfobjects_0000_0017_0002
 - mfobjects/__MIDL___MIDL_itf_mfobjects_0000_0017_0002
 - MF_FILE_OPENMODE
 - mfobjects/MF_FILE_OPENMODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_FILE_OPENMODE
---

# MF_FILE_OPENMODE enumeration


## -description

Specifies how to open or create a file.

## -enum-fields

### -field MF_OPENMODE_FAIL_IF_NOT_EXIST:0

Open an existing file. Fail if the file does not exist.

### -field MF_OPENMODE_FAIL_IF_EXIST:1

Create a new file. Fail if the file already exists.

### -field MF_OPENMODE_RESET_IF_EXIST:2

Open an existing file and truncate it, so that the size is zero bytes. Fail if the file does not already exist.

### -field MF_OPENMODE_APPEND_IF_EXIST:3

If the file does not exist, create a new file. If the file exists, open it.

### -field MF_OPENMODE_DELETE_IF_EXIST:4

Create a new file. If the file exists, overwrite the file.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile">MFCreateFile</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile">MFCreateTempFile</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
