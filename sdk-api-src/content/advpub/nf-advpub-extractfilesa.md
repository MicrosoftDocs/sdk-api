---
UID: NF:advpub.ExtractFilesA
title: ExtractFilesA function
author: windows-sdk-content
description: The ExtractFiles method of the Merge object extracts the embedded .cab file from a module and then writes those files to the destination directory.
old-location: setup\merge_extractfiles.htm
old-project: msi
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ExtractFiles method, ExtractFiles method,Merge object, ExtractFilesA, ExtractFilesW, IMsmMerge.ExtractFiles, Merge object,ExtractFiles method, Merge.ExtractFiles, _msi_extractfiles_method, setup.merge_extractfiles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: advpub.h
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
tech.root: 
req.typenames: AUDIT_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - Merge.ExtractFiles
 - ExtractFilesA
 - ExtractFilesW
 - IMsmMerge.ExtractFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: Mergemod.dll
req.irql: 
---

# ExtractFilesA function


## -description


The 
<b>ExtractFiles</b> method of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a> object extracts the embedded .cab file from a module and then writes those files to the destination directory.


## -parameters




### -param pszCabName

TBD


### -param pszExpandDir

TBD


### -param dwFlags

TBD


### -param pszFileList

TBD


### -param lpReserved

TBD


### -param dwReserved

TBD




#### - Path

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



