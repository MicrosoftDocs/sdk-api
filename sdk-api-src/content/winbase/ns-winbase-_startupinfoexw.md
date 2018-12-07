---
UID: NS:winbase._STARTUPINFOEXW
title: "_STARTUPINFOEXW"
author: windows-sdk-content
description: Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the CreateProcess and CreateProcessAsUser functions.
old-location: base\startupinfoex.htm
tech.root: procthread
ms.assetid: 61203f57-292d-4ea1-88f4-a3b05012d7a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSTARTUPINFOEXW, LPSTARTUPINFOEX, LPSTARTUPINFOEX structure pointer, STARTUPINFOEX, STARTUPINFOEX structure, STARTUPINFOEXA, STARTUPINFOEXW, _STARTUPINFOEXA, _STARTUPINFOEXW, base.startupinfoex, winbase/LPSTARTUPINFOEX, winbase/STARTUPINFOEX, winbase/STARTUPINFOEXA, winbase/STARTUPINFOEXW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: STARTUPINFOEXW (Unicode) and STARTUPINFOEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - STARTUPINFOEX
 - STARTUPINFOEXA
 - STARTUPINFOEXW
product: Windows
targetos: Windows
req.typenames: STARTUPINFOEXW, *LPSTARTUPINFOEXW
req.redist: 
---

# _STARTUPINFOEXW structure


## -description


Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> and 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> functions.


## -struct-fields




### -field StartupInfo

A <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure.


### -field lpAttributeList

An attribute list. This list is created by the <a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a> function.


## -remarks



Be sure to set the <b>cb</b> member of the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure to <code>sizeof(STARTUPINFOEX)</code>.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a>
 

 

