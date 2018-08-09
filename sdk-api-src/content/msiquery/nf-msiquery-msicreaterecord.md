---
UID: NF:msiquery.MsiCreateRecord
title: MsiCreateRecord function
author: windows-sdk-content
description: The MsiCreateRecord function creates a new record object with the specified number of fields. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msicreaterecord.htm
old-project: msi
ms.assetid: fc1d5a09-3097-4a1c-a615-1b93f7eacb04
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MsiCreateRecord, MsiCreateRecord function, _msi_msicreaterecord, msiquery/MsiCreateRecord, setup.msicreaterecord
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
 - MsiCreateRecord
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiCreateRecord function


## -description


The 
<b>MsiCreateRecord</b> function creates a new record object with the specified number of fields. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters




### -param cParams [in]

Specifies the number of fields the record will have. The maximum number of fields in a record is limited to 65535.


## -returns



If the function succeeds, the return value is handle to a new record object.

If the function fails, the return value is null.




## -remarks



Field 0 of the record object created by the 
<b>MsiCreateRecord</b> function is used for format strings and operation codes and is not included in the count specified by <i>cParams</i>. All fields are initialized to null.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="https://msdn.microsoft.com/en-us/library/Bb204770(v=VS.85).aspx">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.




## -see-also




<a href="https://msdn.microsoft.com/95516437-9708-4f4e-a5c2-7bcd4741c776">Database Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Record Processing Functions</a>
 

 

