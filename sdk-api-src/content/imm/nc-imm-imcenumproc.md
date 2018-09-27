---
UID: NC:imm.IMCENUMPROC
title: IMCENUMPROC
author: windows-sdk-content
description: An application-defined callback function that processes input contexts provided by the ImmEnumInputContext function.
old-location: intl\enuminputcontext.htm
tech.root: Intl
ms.assetid: c66dcc0f-733a-44a2-942f-f518b752d014
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EnumInputContext, EnumInputContext callback function [Internationalization for Windows Applications], IMCENUMPROC, IMCENUMPROC callback, _win32_EnumInputContext, imm/EnumInputContext, intl.enuminputcontext
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
 - UserDefined
api_location:
 - Imm.h
api_name:
 - EnumInputContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMCENUMPROC callback function


## -description


An application-defined callback function that processes input contexts provided by the <a href="https://msdn.microsoft.com/b066af9a-5bcc-468b-bc1b-79b549a9e55c">ImmEnumInputContext</a> function. The IMCENUMPROC type defines a pointer to this callback function. <b>EnumInputContext</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - hIMC [in]

Handle to the input context.


#### - lParam [in]

Application-supplied data.


## -returns



Returns a nonzero value to continue enumeration, or 0 to stop enumeration.




## -remarks



An application must register this function by passing its address to the <a href="https://msdn.microsoft.com/b066af9a-5bcc-468b-bc1b-79b549a9e55c">ImmEnumInputContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b066af9a-5bcc-468b-bc1b-79b549a9e55c">ImmEnumInputContext</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

