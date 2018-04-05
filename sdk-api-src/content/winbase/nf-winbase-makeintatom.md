---
UID: NF:winbase.MAKEINTATOM
title: MAKEINTATOM macro
author: windows-driver-content
description: Converts the specified atom into a string, so it can be passed to functions which accept either atoms or strings.
old-location: dataxchg\makeintatom.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atommacros\makeintatom.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbase.h
api_name:
-	MAKEINTATOM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# MAKEINTATOM macro


## -description


Converts the specified atom into a string, so it can be passed to functions which accept either atoms or strings. 


## -parameters




### -param i

TBD






#### - wInteger

The numeric value to be made into an integer atom. This parameter can be either an integer atom or a string atom. 


## -remarks



Although the return value of the <b>MAKEINTATOM</b> macro is cast as an <b>LPTSTR</b> value, it cannot be used as a string pointer except when it is passed to atom-management functions that require an <b>LPTSTR</b> argument. 




## -see-also




<a href="https://msdn.microsoft.com/0712cd2e-397f-48e1-b3bd-ed0dd3155373">AddAtom</a>



<a href="https://msdn.microsoft.com/44c4fbdd-2206-4a6f-9bf1-5495407f6800">DeleteAtom</a>



<a href="https://msdn.microsoft.com/50b01772-660c-4421-8a6f-a6da5369bad4">GetAtomName</a>



<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>



<a href="https://msdn.microsoft.com/387f2dbf-39c3-4294-b77d-0439e296a000">GlobalDeleteAtom</a>



<a href="https://msdn.microsoft.com/7ba8ea4d-7efe-4eb3-afea-c84ab6cacaea">GlobalGetAtomName</a>



<b>Reference</b>
 

 

