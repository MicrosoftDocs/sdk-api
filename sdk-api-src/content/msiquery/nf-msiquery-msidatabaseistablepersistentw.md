---
UID: NF:msiquery.MsiDatabaseIsTablePersistentW
title: MsiDatabaseIsTablePersistentW function
author: windows-sdk-content
description: The MsiDatabaseIsTablePersistent function returns an enumeration that describes the state of a specific table.
old-location: setup\msidatabaseistablepersistent.htm
tech.root: msi
ms.assetid: 78c9d95a-8e36-40a4-afbb-4d0bf5f6f350
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MsiDatabaseIsTablePersistent, MsiDatabaseIsTablePersistent function, MsiDatabaseIsTablePersistentA, MsiDatabaseIsTablePersistentW, _msi_msidatabaseistablepersistent, msiquery/MsiDatabaseIsTablePersistent, msiquery/MsiDatabaseIsTablePersistentA, msiquery/MsiDatabaseIsTablePersistentW, setup.msidatabaseistablepersistent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiDatabaseIsTablePersistentW function


## -description


The 
<b>MsiDatabaseIsTablePersistent</b> function returns an enumeration that describes the state of a specific table.


## -parameters




### -param hDatabase [in]

Handle to the database that belongs to the relevant table. For more information, see <a href="https://msdn.microsoft.com/53cf73bc-4d52-471c-8384-46d106a36e38">Obtaining a Database Handle</a>.


### -param szTableName [in]

Specifies the name of the relevant table.


## -returns



This function returns MSICONDITION.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">General Database Access Functions</a>
 

 

