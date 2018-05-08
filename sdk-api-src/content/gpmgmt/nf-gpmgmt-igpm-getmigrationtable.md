---
UID: NF:gpmgmt.IGPM.GetMigrationTable
title: IGPM::GetMigrationTable
author: windows-driver-content
description: Loads the migration table at a specified path.
old-location: gpmc\igpm_getmigrationtable.htm
old-project: GPMC
ms.assetid: 4a39d4f8-777d-4cf8-8dd5-053f73bdfdfa
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GPM object [GPMC],GetMigrationTable method, GetMigrationTable, GetMigrationTable method [GPMC], GetMigrationTable method [GPMC],GPM object, GetMigrationTable method [GPMC],IGPM interface, IGPM interface [GPMC],GetMigrationTable method, IGPM.GetMigrationTable, IGPM::GetMigrationTable, gpmc.igpm_getmigrationtable, gpmgmt/IGPM::GetMigrationTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPM.GetMigrationTable
-	GPM.GetMigrationTable
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::GetMigrationTable


## -description


Loads the migration table at a specified path.


## -parameters




### -param bstrMigrationTablePath [in]

The path of the migration table to be loaded. Use a null-terminated string.


### -param ppMigrationTable






#### - bstrFilePath [in]

The path of the migration table to be loaded.


#### - ppTable [out]

The migration table interface that contains the entries from the migration table.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMMigrationTable</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMMigrationTable</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/c80c76b0-8589-4ecb-b9bf-6b8377fa98dd">IGPMMigrationTable</a>
 

 

