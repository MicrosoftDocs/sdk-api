---
UID: NF:msiquery.MsiGetDatabaseState
title: MsiGetDatabaseState function (msiquery.h)
author: windows-sdk-content
description: The MsiGetDatabaseState function returns the state of the database.
old-location: setup\msigetdatabasestate.htm
tech.root: Msi
ms.assetid: 33c4618f-f9b5-4512-baba-27f62cd32329
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiGetDatabaseState, MsiGetDatabaseState function, _msi_msigetdatabasestate, msiquery/MsiGetDatabaseState, setup.msigetdatabasestate
ms.topic: function
f1_keywords: ["msiquery/MsiGetDatabaseState"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiGetDatabaseState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiGetDatabaseState function


## -description


The 
<b>MsiGetDatabaseState</b> function returns the state of the database.


## -parameters




### -param hDatabase [in]

Handle to the database obtained from <a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a>.


## -returns



This function returns MSIDBSTATE.




## -remarks



The 
<b>MsiGetDatabaseState</b> function returns the update state of the database.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Database Management Functions</a>
 

 

