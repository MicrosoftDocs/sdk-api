---
UID: NF:gpmgmt.IGPM.CreateMigrationTable
title: IGPM::CreateMigrationTable
author: windows-driver-content
description: Creates an empty migration table.
old-location: gpmc\igpm_createmigrationtable.htm
old-project: GPMC
ms.assetid: ae9ea50f-d652-4d7a-aac5-5b9ef27b99e0
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CreateMigrationTable, CreateMigrationTable method [GPMC], CreateMigrationTable method [GPMC],GPM class, CreateMigrationTable method [GPMC],IGPM interface, GPM class [GPMC],CreateMigrationTable method, IGPM interface [GPMC],CreateMigrationTable method, IGPM.CreateMigrationTable, IGPM::CreateMigrationTable, gpmc.igpm_createmigrationtable, gpmgmt/IGPM::CreateMigrationTable
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
-	IGPM.CreateMigrationTable
-	GPM.CreateMigrationTable
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPM::CreateMigrationTable


## -description


Creates an empty migration table.


## -parameters




### -param ppMigrationTable






#### - ppTable [out]

Receives the created migration table that contains no entries. See <a href="https://msdn.microsoft.com/c80c76b0-8589-4ecb-b9bf-6b8377fa98dd">IGPMMigrationTable</a>.


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
 

 

