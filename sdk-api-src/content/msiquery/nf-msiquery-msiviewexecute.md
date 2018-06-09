---
UID: NF:msiquery.MsiViewExecute
title: MsiViewExecute function
author: windows-sdk-content
description: The MsiViewExecute function executes a SQL view query and supplies any required parameters.
old-location: setup\msiviewexecute.htm
old-project: Msi
ms.assetid: 12b2373f-425a-4035-bdb4-be1a5469f1d7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: MsiViewExecute, MsiViewExecute function, _msi_msiviewexecute, msiquery/MsiViewExecute, setup.msiviewexecute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: InkRecoGuide
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
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiViewExecute function


## -description


The 
<b>MsiViewExecute</b> function executes a SQL view query and supplies any required parameters. The query uses the question mark token to represent parameters as described in 
<a href="https://msdn.microsoft.com/badee528-fa69-43ab-965e-d9e6f2529b99">SQL Syntax</a>. The values of these parameters are passed in as the corresponding fields of a parameter record.


## -parameters




### -param hView [in]

Handle to the view upon which to execute the query.


### -param hRecord [in]

Handle to a record that supplies the parameters. This parameter contains values to replace the parameter tokens in the SQL query. It is optional, so <i>hRecord</i> can be zero. For a reference on syntax, see 
<a href="https://msdn.microsoft.com/badee528-fa69-43ab-965e-d9e6f2529b99">SQL Syntax</a>.


## -returns



Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.




## -remarks



The 
<b>MsiViewExecute</b> function must be called before any calls to 
<a href="https://msdn.microsoft.com/1a973a22-ca3a-4980-9b20-d3c5b43fdd19">MsiViewFetch</a>.

If the SQL query specifies values with parameter markers (?), a record must be supplied that contains all of the replacement values in the exact order and of compatible data types. When used with INSERT and UPDATE queries all the parameterized values must precede all nonparameterized values.

For example, these queries are valid.

UPDATE {table-list} SET {column}= ? , {column}= {constant}

INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})

However these queries are invalid.

UPDATE {table-list} SET {column}= {constant}, {column}=?

INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ? )

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop//Msi/database-functions">General Database Access Functions</a>
 

 

