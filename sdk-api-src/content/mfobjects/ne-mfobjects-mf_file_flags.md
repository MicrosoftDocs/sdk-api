---
UID: NE:mfobjects.__MIDL___MIDL_itf_mfobjects_0000_0017_0003
title: MF_FILE_FLAGS (mfobjects.h)
description: Specifies the behavior when opening a file.
helpviewer_keywords: ["1e1c906e-c832-4df1-96f5-86e690c3c34e","MF_FILEFLAGS_ALLOW_WRITE_SHARING","MF_FILEFLAGS_NOBUFFERING","MF_FILEFLAGS_NONE","MF_FILE_FLAGS","MF_FILE_FLAGS enumeration [Media Foundation]","mf.mf_file_flags","mfobjects/MF_FILEFLAGS_ALLOW_WRITE_SHARING","mfobjects/MF_FILEFLAGS_NOBUFFERING","mfobjects/MF_FILEFLAGS_NONE","mfobjects/MF_FILE_FLAGS"]
old-location: mf\mf_file_flags.htm
tech.root: mf
ms.assetid: 1e1c906e-c832-4df1-96f5-86e690c3c34e
ms.date: 12/05/2018
ms.keywords: 1e1c906e-c832-4df1-96f5-86e690c3c34e, MF_FILEFLAGS_ALLOW_WRITE_SHARING, MF_FILEFLAGS_NOBUFFERING, MF_FILEFLAGS_NONE, MF_FILE_FLAGS, MF_FILE_FLAGS enumeration [Media Foundation], mf.mf_file_flags, mfobjects/MF_FILEFLAGS_ALLOW_WRITE_SHARING, mfobjects/MF_FILEFLAGS_NOBUFFERING, mfobjects/MF_FILEFLAGS_NONE, mfobjects/MF_FILE_FLAGS
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
req.typenames: MF_FILE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mfobjects_0000_0017_0003
 - mfobjects/__MIDL___MIDL_itf_mfobjects_0000_0017_0003
 - MF_FILE_FLAGS
 - mfobjects/MF_FILE_FLAGS
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
 - MF_FILE_FLAGS
---

# MF_FILE_FLAGS enumeration


## -description

Specifies the behavior when opening a file.

## -enum-fields

### -field MF_FILEFLAGS_NONE:0

Use the default behavior.

### -field MF_FILEFLAGS_NOBUFFERING:0x1

Open the file with no system caching.

### -field MF_FILEFLAGS_ALLOW_WRITE_SHARING:0x2

Subsequent open operations can have write access to the file.



<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfbegincreatefile">MFBeginCreateFile</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile">MFCreateFile</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile">MFCreateTempFile</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
