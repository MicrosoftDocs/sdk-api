---
UID: NF:gpmgmt.IGPMMigrationTable.GetEntries
title: IGPMMigrationTable::GetEntries
author: windows-sdk-content
description: Returns a IGPMMapEntryCollection interface.
old-location: gpmc\igpmmigrationtable_getentries.htm
old-project: GPMC
ms.assetid: 5de22bba-10f9-49f7-83f3-053f5e58b66e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMMigrationTable class [GPMC],GetEntries method, GetEntries, GetEntries method [GPMC], GetEntries method [GPMC],GPMMigrationTable class, GetEntries method [GPMC],IGPMMigrationTable interface, IGPMMigrationTable interface [GPMC],GetEntries method, IGPMMigrationTable.GetEntries, IGPMMigrationTable::GetEntries, gpmc.igpmmigrationtable_getentries, gpmgmt/IGPMMigrationTable::GetEntries
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.GetEntries
 - GPMMigrationTable.GetEntries
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMMigrationTable::GetEntries


## -description


Returns a <b>IGPMMapEntryCollection</b> interface.


## -parameters




### -param ppEntries [out]

The list of entries in the migration table.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/a017ff4b-ab3c-4da9-b6c9-b4ccd24230eb">GPMMapEntryCollection</a> object.

<h3>VB</h3>
Returns a reference to a <a href="https://msdn.microsoft.com/a017ff4b-ab3c-4da9-b6c9-b4ccd24230eb">GPMMapEntryCollection</a> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMMigrationTable</a>
 

 

