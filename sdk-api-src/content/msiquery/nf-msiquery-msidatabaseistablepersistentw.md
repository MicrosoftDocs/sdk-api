---
UID: NF:msiquery.MsiDatabaseIsTablePersistentW
title: MsiDatabaseIsTablePersistentW function (msiquery.h)
description: The MsiDatabaseIsTablePersistent function returns an enumeration that describes the state of a specific table. (Unicode)
helpviewer_keywords: ["MsiDatabaseIsTablePersistent", "MsiDatabaseIsTablePersistent function", "MsiDatabaseIsTablePersistentW", "_msi_msidatabaseistablepersistent", "msiquery/MsiDatabaseIsTablePersistent", "msiquery/MsiDatabaseIsTablePersistentW", "setup.msidatabaseistablepersistent"]
old-location: setup\msidatabaseistablepersistent.htm
tech.root: setup
ms.assetid: 78c9d95a-8e36-40a4-afbb-4d0bf5f6f350
ms.date: 12/05/2018
ms.keywords: MsiDatabaseIsTablePersistent, MsiDatabaseIsTablePersistent function, MsiDatabaseIsTablePersistentA, MsiDatabaseIsTablePersistentW, _msi_msidatabaseistablepersistent, msiquery/MsiDatabaseIsTablePersistent, msiquery/MsiDatabaseIsTablePersistentA, msiquery/MsiDatabaseIsTablePersistentW, setup.msidatabaseistablepersistent
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDatabaseIsTablePersistentW (Unicode) and MsiDatabaseIsTablePersistentA (ANSI)
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
 - MsiDatabaseIsTablePersistentW
 - msiquery/MsiDatabaseIsTablePersistentW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiDatabaseIsTablePersistent
 - MsiDatabaseIsTablePersistentA
 - MsiDatabaseIsTablePersistentW
---

# MsiDatabaseIsTablePersistentW function


## -description

The 
<b>MsiDatabaseIsTablePersistent</b> function returns an enumeration that describes the state of a specific table.

## -parameters

### -param hDatabase [in]

Handle to the database that belongs to the relevant table. For more information, see <a href="/windows/desktop/Msi/obtaining-a-database-handle">Obtaining a Database Handle</a>.

### -param szTableName [in]

Specifies the name of the relevant table.

## -returns

This function returns MSICONDITION.

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>

## -remarks

> [!NOTE]
> The msiquery.h header defines MsiDatabaseIsTablePersistent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
