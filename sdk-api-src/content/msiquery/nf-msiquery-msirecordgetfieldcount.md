---
UID: NF:msiquery.MsiRecordGetFieldCount
title: MsiRecordGetFieldCount function (msiquery.h)
description: Returns the number of fields in a record.
helpviewer_keywords: ["MsiRecordGetFieldCount","MsiRecordGetFieldCount function","_msi_msirecordgetfieldcount","msiquery/MsiRecordGetFieldCount","setup.msirecordgetfieldcount"]
old-location: setup\msirecordgetfieldcount.htm
tech.root: setup
ms.assetid: 17d4e593-f80c-4f67-bfd0-fa487e2477c4
ms.date: 12/05/2018
ms.keywords: MsiRecordGetFieldCount, MsiRecordGetFieldCount function, _msi_msirecordgetfieldcount, msiquery/MsiRecordGetFieldCount, setup.msirecordgetfieldcount
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista.
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
 - MsiRecordGetFieldCount
 - msiquery/MsiRecordGetFieldCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiRecordGetFieldCount
---

# MsiRecordGetFieldCount function


## -description

The 
<b>MsiRecordGetFieldCount</b> function returns the number of fields in a record.

## -parameters

### -param hRecord [in]

Handle to a record.

## -returns

If the function succeeds, the return value is the number of fields in the record.

## -remarks

The count returned by the 
<b>MsiRecordGetFieldCount</b> parameter does not include field 0. Read access to fields beyond this count returns null values. Write access fails.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>