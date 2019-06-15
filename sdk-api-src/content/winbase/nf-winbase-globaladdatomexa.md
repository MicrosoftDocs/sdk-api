---
UID: NF:winbase.GlobalAddAtomExA
title: GlobalAddAtomExA function (winbase.h)
author: windows-sdk-content
description: Adds a character string to the global atom table and returns a unique value (an atom) identifying the string.
old-location: dataxchg\globaladdatomex.htm
tech.root: dataxchg
ms.assetid: C5D982F5-94A9-4B08-AE07-8F40E4128123
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GlobalAddAtomEx, GlobalAddAtomEx function [Data Exchange], GlobalAddAtomExA, GlobalAddAtomExW, dataxchg.globaladdatomex, winbase/GlobalAddAtomEx, winbase/GlobalAddAtomExA, winbase/GlobalAddAtomExW
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GlobalAddAtomExW (Unicode) and GlobalAddAtomExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GlobalAddAtomEx
 - GlobalAddAtomExA
 - GlobalAddAtomExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GlobalAddAtomExA function


## -description


Adds a character string to the global atom table and returns a unique value (an atom) identifying the string.


## -parameters




### -param lpString [in, optional]

The null-terminated string to be added. The string can have a maximum size of 255 bytes. Strings that differ only in case are considered identical. The case of the first string of this name added to the table is preserved and returned by the <a href="https://msdn.microsoft.com/7ba8ea4d-7efe-4eb3-afea-c84ab6cacaea">GlobalGetAtomName</a> function.

Alternatively, you can use an integer atom that has been converted using the <a href="https://msdn.microsoft.com/11270568-ef0e-4bed-9e07-cb62773178ff">MAKEINTATOM</a> macro. See the Remarks for more information. 


### -param Flags [in]


## -returns



If the function succeeds, the return value is the newly created atom.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/890c8c69-5a8e-42be-9eaf-84f9ccaa7e3d">GlobalAddAtom</a>
 

 

