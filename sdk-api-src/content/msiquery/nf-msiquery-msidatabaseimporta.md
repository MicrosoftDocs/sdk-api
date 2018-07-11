---
UID: NF:msiquery.MsiDatabaseImportA
title: MsiDatabaseImportA function
author: windows-sdk-content
description: The MsiDatabaseImport function imports an installer text archive file into an open database table.
old-location: setup\msidatabaseimport.htm
old-project: msi
ms.assetid: df277641-393e-4202-bb92-4b813ddaa0ca
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: MsiDatabaseImport, MsiDatabaseImport function, MsiDatabaseImportA, MsiDatabaseImportW, _msi_msidatabaseimport, msiquery/MsiDatabaseImport, msiquery/MsiDatabaseImportA, msiquery/MsiDatabaseImportW, setup.msidatabaseimport
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
req.unicode-ansi: MsiDatabaseImportW (Unicode) and MsiDatabaseImportA (ANSI)
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
api_name:
 - MsiDatabaseImport
 - MsiDatabaseImportA
 - MsiDatabaseImportW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiDatabaseImportA function


## -description


The 
<b>MsiDatabaseImport</b> function imports an installer <a href="https://msdn.microsoft.com/49210242-bd32-4e5c-b782-a132d670fdfe">text archive file</a>  into an open database table.


## -parameters




### -param hDatabase [in]

Handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>.


### -param szFolderPath [in]

Specifies the path to the folder that contains archive files.


### -param szFileName [in]

Specifies the name of the file to import.


## -returns




					The 
<b>MsiDatabaseImport</b> function returns one of the following values:




## -remarks



When you use the 
<b>MsiDatabaseImport</b> function to import a text archive table named _SummaryInformation into an installer database, you write the "05SummaryInformation" stream. This stream contains standard properties that can be viewed using Windows Explorer and are defined by COM. The rows of the table are written to the property stream as pairs of property ID numbers and corresponding data values. See 
<a href="https://msdn.microsoft.com/a5dd014f-21af-41f9-be75-1b139946179d">Summary Information Stream Property Set</a>. Date and time in _SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss. For example, 1999/03/22 15:25:45. If the table contains binary streams, the name of the stream is in the data field, and the actual stream is retrieved from a file of that name in a subfolder with the same name as the table.

Text archive files that are exported from a database by 
<a href="https://msdn.microsoft.com/c20c168d-900e-496a-894c-5678f308cdbe">MsiDatabaseExport</a> are intended for use with version control systems, and are not intended to be used as a means of editing data. Use the database API functions and tools designed for that purpose. Note that control characters in text archive files are translated to avoid conflicts with file delimiters. If a text archive file contains non-ASCII data, it is stamped with the code page of the data, and can only be imported into a database of that exact code page, or into a neutral database. Neutral databases are set to the code page of the imported file. A database can be unconditionally set to a particular code page by importing a pseudo table named: _ForceCodepage. The format of such a file is: Two blank lines, followed by a line that contains the numeric code page, a tab delimiter and the exact string: _ForceCodepage

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">Database Management Functions</a>



<a href="https://msdn.microsoft.com/49210242-bd32-4e5c-b782-a132d670fdfe">Text Archive Files </a>
 

 

