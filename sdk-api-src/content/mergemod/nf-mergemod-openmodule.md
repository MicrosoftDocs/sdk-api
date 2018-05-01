---
UID: NF:mergemod.OpenModule
title: OpenModule function
author: windows-driver-content
description: The OpenModule method of the Merge object opens a Windows Installer merge module in read-only mode. A module must be opened before it can be merged with an installation database.
old-location: setup\merge_openmodule.htm
old-project: Msi
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: Merge class, OpenModule method, OpenModule, OpenModule method, OpenModule method, Merge class, _msi_openmodule_method, setup.merge_openmodule
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
-	Merge.OpenModule
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
req.product: GDI+ 1.1
---

# OpenModule function


## -description


The 
<b>OpenModule</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object opens a Windows Installer merge module in read-only mode. A module must be opened before it can be merged with an installation database.


## -parameters




### -param Path

TBD


### -param Language

A valid language identifier (LANGID).


#### - FileName

Fully qualified file name pointing to a merge module.


## -returns



This method does not return a value.




## -remarks



This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the 
<a href="https://msdn.microsoft.com/a11f72cf-4c4e-4650-95f9-549169452622">CloseModule</a> method is called.

The installer attempts to open the module in the language specified by <i>Language</i>, or a more general language. For example, if <i>Language</i> is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language. A <i>Language</i> value of 9 opens modules with a default language of 9 or 0. If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language. If that fails, the module is transformed to increasingly general languages, all the way to language neutral. If none of the transforms succeed, the module fails to open. In this case, an error is added to the error list of type msmErrorLanguageUnsupported. If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed. For details, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object. Opening a merge module clears any errors that have not already been retrieved.

<h3><a id="C__"></a><a id="c__"></a>C++</h3>
See 
<a href="https://msdn.microsoft.com/37225e61-c24f-4a44-8fdf-673590a6e09d">OpenModule</a> function.



