---
UID: NF:mergemod.Merge
title: Merge function
author: windows-driver-content
description: The Merge method of the Merge object executes a merge of the current database and current module.
old-location: setup\merge_merge.htm
old-project: Msi
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: Merge, Merge class, Merge method, Merge method, Merge method, Merge class, _msi_merge_method_merge_object_, setup.merge_merge
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
-	Merge.Merge
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# Merge function


## -description


The 
<b>Merge</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object executes a merge of the current database and current module. The merge attaches the components in the module to the feature identified by <i>Feature</i>. The root of the module's directory tree is redirected to the location given by <i>RedirectDir</i>.

The 
<b>Merge</b> method can only be called once to merge a particular combination of .msi and .msm files.


## -parameters




### -param Feature

The name of a feature in the database.


### -param RedirectDir

The key of an entry in the 
<a href="https://msdn.microsoft.com/eaca30cb-fec1-49ca-8b23-5e54c583e3e2">Directory table</a> of the database. This parameter may be null or an empty string.


## -returns



This method does not return a value.




## -remarks



Once the merge is complete, components in the module are attached to the feature identified by <i>Feature</i>. This feature is not created and must be an existing feature. Note that the 
<b>Merge</b> method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database. For more information, see 
<a href="https://msdn.microsoft.com/f2891457-efef-4319-bd09-5de7fcf32d21">Referencing Features in Merge Modules</a>.

The module may be attached to additional features using the 
<a href="https://msdn.microsoft.com/1c1ef664-792c-4cdc-b468-1ffe0b7810a5">Connect</a> method. Note that calling the 
<b>Connect</b> method only creates feature-component associations. It does not modify the rows that have already been merged in to the database.

Changes made to the database are saved if and only if the 
<a href="https://msdn.microsoft.com/efbb6238-e9e3-4603-896a-75fcff2bb362">CloseDatabase</a> method is called with <i>bCommit</i> set to <b>TRUE</b>.

If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail. Errors may be retrieved through the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Errors</a> property. Errors and informational messages are posted to the current log file.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> function.



