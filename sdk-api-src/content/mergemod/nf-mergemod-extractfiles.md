---
UID: NF:mergemod.ExtractFiles
title: ExtractFiles function
author: windows-driver-content
description: The ExtractFiles method of the Merge object extracts the embedded .cab file from a module and then writes those files to the destination directory.
old-location: setup\merge_extractfiles.htm
old-project: Msi
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ExtractFiles, ExtractFiles method, ExtractFiles method, Merge class, Merge class, ExtractFiles method, _msi_extractfiles_method, setup.merge_extractfiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mergemod.h
req.include-header: Mergemod.h
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
-	Merge.ExtractFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# ExtractFiles function


## -description


The 
<b>ExtractFiles</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object extracts the embedded .cab file from a module and then writes those files to the destination directory.


## -parameters




### -param Path

The fully qualified destination directory.


## -returns



This method does not return a value.




## -remarks



Any files in the destination directory with the same name are overwritten. The path is created if it does not already exist.

<b>ExtractFiles</b> always extracts files using short file names for the path. To use long file names for the path, use the 
<a href="https://msdn.microsoft.com/8b063052-4f92-466a-9c52-bda26ed13d5c">ExtractFilesEx method</a>.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/e5bafd2d-0750-4aa6-87e8-22ef3cfdd5ff">ExtractFiles</a> function.



