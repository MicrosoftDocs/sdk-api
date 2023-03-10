---
UID: NS:msi._MSIFILEHASHINFO
title: MSIFILEHASHINFO (msi.h)
description: The MSIFILEHASHINFO structure contains the file hash information returned by MsiGetFileHash and used in the MsiFileHash table.
helpviewer_keywords: ["*PMSIFILEHASHINFO","MSIFILEHASHINFO","MSIFILEHASHINFO structure","PMSIFILEHASHINFO","PMSIFILEHASHINFO structure pointer","_msi_msifilehashinfo","msi/MSIFILEHASHINFO","msi/PMSIFILEHASHINFO","setup.msifilehashinfo"]
old-location: setup\msifilehashinfo.htm
tech.root: setup
ms.assetid: b4176b5b-149d-4542-9a6c-27281877a3ff
ms.date: 12/05/2018
ms.keywords: '*PMSIFILEHASHINFO, MSIFILEHASHINFO, MSIFILEHASHINFO structure, PMSIFILEHASHINFO, PMSIFILEHASHINFO structure pointer, _msi_msifilehashinfo, msi/MSIFILEHASHINFO, msi/PMSIFILEHASHINFO, setup.msifilehashinfo'
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
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
req.typenames: MSIFILEHASHINFO, *PMSIFILEHASHINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSIFILEHASHINFO
 - msi/_MSIFILEHASHINFO
 - PMSIFILEHASHINFO
 - msi/PMSIFILEHASHINFO
 - MSIFILEHASHINFO
 - msi/MSIFILEHASHINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msi.h
api_name:
 - MSIFILEHASHINFO
---

# MSIFILEHASHINFO structure


## -description

The 
<b>MSIFILEHASHINFO</b> structure contains the file hash information returned by 
<a href="/windows/desktop/api/msi/nf-msi-msigetfilehasha">MsiGetFileHash</a> and used in the 
<a href="/windows/desktop/Msi/msifilehash-table">MsiFileHash table</a>.

## -struct-fields

### -field dwFileHashInfoSize

Specifies the size, in bytes, of this data structure. Set this member to <code>sizeof(MSIFILEHASHINFO)</code> before calling the 
<a href="/windows/desktop/api/msi/nf-msi-msigetfilehasha">MsiGetFileHash</a> function.

### -field dwData

The entire 128-bit file hash is contained in four 32-bit fields. The first field corresponds to the HashPart1 column of the MsiHashFile table, the second field corresponds to the HashPart2 column, the third field corresponds to the HashPart3 column, and the fourth field corresponds to the HashPart4 column.

## -remarks

The file hash entered into the fields of the MsiFileHash table must be obtained by calling 
<a href="/windows/desktop/api/msi/nf-msi-msigetfilehasha">MsiGetFileHash</a> or the 
<a href="/windows/desktop/Msi/installer-filehash">FileHash method</a>. Do not use other methods to generate a file hash.

## -see-also

<a href="/windows/desktop/Msi/default-file-versioning">Default File Versioning</a>



<a href="/windows/desktop/Msi/msifilehash-table">MsiFileHash table</a>



<a href="/windows/desktop/api/msi/nf-msi-msigetfilehasha">MsiGetFileHash</a>