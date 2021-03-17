---
UID: NF:msiquery.MsiRecordDataSize
title: MsiRecordDataSize function (msiquery.h)
description: The MsiRecordDataSize function returns the length of a record field. The count does not include the terminating null character.
helpviewer_keywords: ["MsiRecordDataSize","MsiRecordDataSize function","_msi_msirecorddatasize","msiquery/MsiRecordDataSize","setup.msirecorddatasize"]
old-location: setup\msirecorddatasize.htm
tech.root: setup
ms.assetid: e0e4e842-697f-43fa-8012-dd911bf3eebc
ms.date: 12/05/2018
ms.keywords: MsiRecordDataSize, MsiRecordDataSize function, _msi_msirecorddatasize, msiquery/MsiRecordDataSize, setup.msirecorddatasize
req.header: msiquery.h
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiRecordDataSize
 - msiquery/MsiRecordDataSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiRecordDataSize
---

# MsiRecordDataSize function


## -description

The 
<b>MsiRecordDataSize</b> function returns the length of a record field. The count does not include the terminating null character.

## -parameters

### -param hRecord [in]

Handle to the record.

### -param iField [in]

Specifies a field of the record.

## -returns

The 
<b>MsiRecordDataSize</b> function returns 0 if the field is null, nonexistent, or an internal object pointer. The function also returns 0 if the handle is not a valid record handle.

If the data is in integer format, the function returns sizeof(int).

If the data is in string format, the function returns the character count (not including the null character).

If the data is in stream format, the function returns the byte count.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>