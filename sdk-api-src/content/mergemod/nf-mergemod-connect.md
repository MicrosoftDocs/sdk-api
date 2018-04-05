---
UID: NF:mergemod.Connect
title: Connect function
author: windows-driver-content
description: The Connect method of the Merge object connects a module to an additional feature. The module must have already been merged into the database or will be merged into the database. The feature must exist before calling this function.
old-location: setup\merge_connect.htm
old-project: Msi
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Connect, Connect method, Connect method, Merge object, Merge object, Connect method, _msi_connect_method, setup.merge_connect
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
-	Merge.Connect
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# Connect function


## -description


The 
<b>Connect</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object connects a module to an additional feature. The module must have already been merged into the database or will be merged into the database. The feature must exist before calling this function.

Changes made to the database are not saved to disk unless the 
<a href="https://msdn.microsoft.com/a89fe77a-0099-4c49-b484-c05ee351a66a">CloseDatabase</a> method is called with <i>bCommit</i> set to <b>TRUE</b>.


## -parameters




### -param Feature

The name of a feature already existing in the database.


## -returns



This method does not return a value.




## -remarks



Errors may be retrieved through the 
<a href="https://msdn.microsoft.com/619f17cc-131a-4262-ad48-9ab1318142aa">Errors</a> property. Errors and informational messages are posted to the current log file.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/f491beb8-90f7-4e41-891d-ef674306339d">Connect</a> function.



