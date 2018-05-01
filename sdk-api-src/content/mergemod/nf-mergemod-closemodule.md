---
UID: NF:mergemod.CloseModule
title: CloseModule function
author: windows-driver-content
description: The CloseModule method of the Merge object closes the currently open Windows Installer merge module.
old-location: setup\merge_closemodule.htm
old-project: Msi
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CloseModule, CloseModule method, CloseModule method, Merge class, Merge class, CloseModule method, _msi_closemodule_method, setup.merge_closemodule
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
-	Merge.CloseModule
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# CloseModule function


## -description


The 
<b>CloseModule</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object closes the currently open Windows Installer merge module.


## -parameters






## -returns



This method does not return a value.




## -remarks



Closing a merge module will not affect any errors that have not been retrieved.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/bbe8ab14-3d8e-441c-a9bf-0319a9b3a5de">CloseModule</a> function.



