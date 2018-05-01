---
UID: NF:mergemod.CloseDatabase
title: CloseDatabase function
author: windows-driver-content
description: The CloseDatabase method of the Merge object closes the currently open Windows Installer database.
old-location: setup\merge_closedatabase.htm
old-project: Msi
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CloseDatabase, CloseDatabase method, CloseDatabase method, Merge class, Merge class, CloseDatabase method, _msi_closedatabase_method, setup.merge_closedatabase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mergemod.dll
api_name:
-	Merge.CloseDatabase
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# CloseDatabase function


## -description


The 
<b>CloseDatabase</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object closes the currently open Windows Installer database.


## -parameters




### -param Commit

TBD




#### - bCommit

<b>TRUE</b> if changes should be saved, <b>FALSE</b> otherwise.


## -returns



This method does not return a value.




## -remarks



Closing a database clears all dependency information but does not affect any errors that have not been retrieved.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/efbb6238-e9e3-4603-896a-75fcff2bb362">CloseDatabase</a> function.



