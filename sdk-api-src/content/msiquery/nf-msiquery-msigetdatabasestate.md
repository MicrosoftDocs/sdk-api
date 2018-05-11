---
UID: NF:msiquery.MsiGetDatabaseState
title: MsiGetDatabaseState function
author: windows-driver-content
description: The MsiGetDatabaseState function returns the state of the database.
old-location: setup\msigetdatabasestate.htm
old-project: Msi
ms.assetid: 33c4618f-f9b5-4512-baba-27f62cd32329
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MsiGetDatabaseState, MsiGetDatabaseState function, _msi_msigetdatabasestate, msiquery/MsiGetDatabaseState, setup.msigetdatabasestate
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiGetDatabaseState
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiGetDatabaseState function


## -description


The 
<b>MsiGetDatabaseState</b> function returns the state of the database.


## -parameters




### -param hDatabase [in]

Handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>.


## -returns



This function returns MSIDBSTATE.




## -remarks



The 
<b>MsiGetDatabaseState</b> function returns the update state of the database.




## -see-also




<a href="database_functions.htm">Database Management Functions</a>
 

 

