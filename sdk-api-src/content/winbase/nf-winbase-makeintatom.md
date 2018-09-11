---
UID: NF:winbase.MAKEINTATOM
title: MAKEINTATOM macro
author: windows-sdk-content
description: Converts the specified atom into a string, so it can be passed to functions which accept either atoms or strings.
old-location: dataxchg\makeintatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atommacros\makeintatom.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MAKEINTATOM, MAKEINTATOM macro [Data Exchange], _win32_MAKEINTATOM, _win32_makeintatom_cpp, dataxchg.makeintatom, winbase/MAKEINTATOM, winui._win32_makeintatom
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - Winbase.h
api_name:
 - MAKEINTATOM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKEINTATOM macro


## -description


Converts the specified atom into a string, so it can be passed to functions which accept either atoms or strings. 


## -parameters




### -param i

The numeric value to be made into an integer atom. This parameter can be either an integer atom or a string atom. 


## -remarks



Although the return value of the <b>MAKEINTATOM</b> macro is cast as an <b>LPTSTR</b> value, it cannot be used as a string pointer except when it is passed to atom-management functions that require an <b>LPTSTR</b> argument. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms649056(v=VS.85).aspx">AddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649057(v=VS.85).aspx">DeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649059(v=VS.85).aspx">GetAtomName</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649060(v=VS.85).aspx">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649061(v=VS.85).aspx">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649063(v=VS.85).aspx">GlobalGetAtomName</a>



<b>Reference</b>
 

 

