---
UID: NF:mergemod.ExtractCAB
title: ExtractCAB function
author: windows-driver-content
description: The ExtractCAB method of the Merge object extracts the embedded .cab file from a module and saves it as the specified file. The installer creates this file if it does not already exist and overwritten if it does exist.
old-location: setup\merge_extractcab.htm
old-project: Msi
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ExtractCAB, ExtractCAB method, ExtractCAB method, Merge class, Merge class, ExtractCAB method, _msi_extractcab_method, setup.merge_extractcab
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
-	Merge.ExtractCAB
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# ExtractCAB function


## -description


The 
<b>ExtractCAB</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object extracts the embedded .cab file from a module and saves it as the specified file. The installer creates this file if it does not already exist and overwritten if it does exist.


## -parameters




### -param FileName

The fully qualified destination file.


## -returns



This method does not return a value.



