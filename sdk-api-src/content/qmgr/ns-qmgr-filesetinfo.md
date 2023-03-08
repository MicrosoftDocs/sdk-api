---
UID: NS:qmgr._FILESETINFO
title: FILESETINFO (qmgr.h)
description: The FILESETINFO structure identifies the remote and local names of the file to download.
helpviewer_keywords: ["FILESETINFO","FILESETINFO structure [BITS]","bits.filesetinfo","qmgr/FILESETINFO"]
old-location: bits\filesetinfo.htm
tech.root: Bits
ms.assetid: 1a1d6683-5317-4a34-828d-55142f64f19f
ms.date: 12/05/2018
ms.keywords: FILESETINFO, FILESETINFO structure [BITS], bits.filesetinfo, qmgr/FILESETINFO
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FILESETINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILESETINFO
 - qmgr/_FILESETINFO
 - FILESETINFO
 - qmgr/FILESETINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qmgr.h
api_name:
 - FILESETINFO
---

# FILESETINFO structure


## -description

<p class="CCE_Message">[Queue Manager (QMGR) is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/background-intelligent-transfer-service-portal">Background Intelligent Transfer Service (BITS)</a>.]

The <b>FILESETINFO</b> structure identifies the remote and local names of the file to download.

## -struct-fields

### -field bstrRemoteFile

Null-terminated string that contains the name of the file on the server (for example, <b>http://</b><i>ServerName</i><b>/</b><i>Path</i><b>/</b><i>FileName</i><b>.</b><i>ext</i>). The format of the name must conform to the transfer protocol you use. You cannot use wildcards in the path or file name. The URL must only contain legal URL characters; no escape processing is performed. The URL is limited to 2,200 characters, not including the terminating null character.

### -field bstrLocalFile

Null-terminated string that contains the name of the file on the client. The file name must include the full path, for example, <b>D:\\</b><i>MyApp</i><b>\\</b><i>UpdatesPath</i><b>\\</b><i>FileName</i><b>.</b><i>ext</i>. You cannot use wildcards in the path or file name, and directories in the path must exist. The path is limited to MAX_PATH, not including the terminating null character. The user must have permission to write to the local directory for downloads and uploads that request a reply. BITS does not support NTFS streams. Instead of using network drives, which are session specific, use UNC paths (for example, <b>\\</b><i>ServerName</i><b>\\</b><i>ShareName</i><b>\\</b><i>Path</i><b>\\</b><i>FileName</i><b>.</b><i>ext</i>).

### -field dwSizeHint

Not supported.