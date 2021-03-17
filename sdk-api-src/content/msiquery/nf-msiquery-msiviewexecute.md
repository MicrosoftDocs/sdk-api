---
UID: NF:msiquery.MsiViewExecute
title: MsiViewExecute function (msiquery.h)
description: The MsiViewExecute function executes a SQL view query and supplies any required parameters.
helpviewer_keywords: ["MsiViewExecute","MsiViewExecute function","_msi_msiviewexecute","msiquery/MsiViewExecute","setup.msiviewexecute"]
old-location: setup\msiviewexecute.htm
tech.root: setup
ms.assetid: 12b2373f-425a-4035-bdb4-be1a5469f1d7
ms.date: 12/05/2018
ms.keywords: MsiViewExecute, MsiViewExecute function, _msi_msiviewexecute, msiquery/MsiViewExecute, setup.msiviewexecute
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
 - MsiViewExecute
 - msiquery/MsiViewExecute
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
 - MsiViewExecute
---

# MsiViewExecute function


## -description

The 
<b>MsiViewExecute</b> function executes a SQL view query and supplies any required parameters. The query uses the question mark token to represent parameters as described in 
<a href="/windows/desktop/Msi/sql-syntax">SQL Syntax</a>. The values of these parameters are passed in as the corresponding fields of a parameter record.

## -parameters

### -param hView [in]

Handle to the view upon which to execute the query.

### -param hRecord [in]

Handle to a record that supplies the parameters. This parameter contains values to replace the parameter tokens in the SQL query. It is optional, so <i>hRecord</i> can be zero. For a reference on syntax, see 
<a href="/windows/desktop/Msi/sql-syntax">SQL Syntax</a>.

## -returns

Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.

## -remarks

The 
<b>MsiViewExecute</b> function must be called before any calls to 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a>.

If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values in the exact order and of compatible data types. When used with INSERT and UPDATE queries all the parameterized values must precede all nonparameterized values.

For example, these queries are valid.

UPDATE {table-list} SET {column}= ? , {column}= {constant}

INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})

However these queries are invalid.

UPDATE {table-list} SET {column}= {constant}, {column}=?

INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ? )

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>