---
UID: NC:imm.REGISTERWORDENUMPROCA
title: REGISTERWORDENUMPROCA
author: windows-sdk-content
description: An application-defined callback function used with the ImmEnumRegisterWord function.
old-location: intl\enumregisterwordproc.htm
tech.root: Intl
ms.assetid: 06038c87-3553-47de-ba9f-b9c65ea9920b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnumRegisterWordProc, EnumRegisterWordProc callback function [Internationalization for Windows Applications], EnumRegisterWordProcA, EnumRegisterWordProcW, REGISTERWORDENUMPROC, REGISTERWORDENUMPROC callback, REGISTERWORDENUMPROCA, REGISTERWORDENUMPROCW, _win32_EnumRegisterWordProc, imm/EnumRegisterWordProc, imm/EnumRegisterWordProcA, imm/EnumRegisterWordProcW, intl.enumregisterwordproc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumRegisterWordProcW (Unicode) and EnumRegisterWordProcA (ANSI)
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
 - UserDefined
api_location:
 - Imm.h
api_name:
 - EnumRegisterWordProc
 - EnumRegisterWordProcA
 - EnumRegisterWordProcW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# REGISTERWORDENUMPROCA callback function


## -description


An application-defined callback function used with the <a href="https://msdn.microsoft.com/ebeed3f9-1164-49d8-a7af-61244976643b">ImmEnumRegisterWord</a> function. It is used to process data of register strings. The REGISTERWORDENUMPROC type defines a pointer to this callback function. <b>EnumRegisterWordProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param lpszReading [in]

Pointer to a null-terminated string specifying the matched reading string.


### -param Arg1


### -param lpszString [in]

Pointer to a null-terminated string specifying the matched register string.


### -param Arg2








#### - dwStyle [in]

The style of the register string.


#### - lpData [in]

Application-supplied data.


## -returns



Returns a nonzero value to continue enumeration, or 0 to stop enumeration.




## -remarks



An application must register this function by passing its address to the <a href="https://msdn.microsoft.com/ebeed3f9-1164-49d8-a7af-61244976643b">ImmEnumRegisterWord</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ebeed3f9-1164-49d8-a7af-61244976643b">ImmEnumRegisterWord</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

