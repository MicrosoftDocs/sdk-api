---
UID: NC:imm.IMCENUMPROC
title: IMCENUMPROC (imm.h)
description: IMCENUMPROC (imm.h) is an application-defined callback function that processes input contexts provided by the ImmEnumInputContext function.
helpviewer_keywords: ["EnumInputContext","EnumInputContext callback function [Internationalization for Windows Applications]","IMCENUMPROC","IMCENUMPROC callback","_win32_EnumInputContext","imm/EnumInputContext","intl.enuminputcontext"]
old-location: intl\enuminputcontext.htm
tech.root: Intl
ms.assetid: c66dcc0f-733a-44a2-942f-f518b752d014
ms.date: 08/04/2022
ms.keywords: EnumInputContext, EnumInputContext callback function [Internationalization for Windows Applications], IMCENUMPROC, IMCENUMPROC callback, _win32_EnumInputContext, imm/EnumInputContext, intl.enuminputcontext
req.header: imm.h
req.include-header: Immdev.h, Windows.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMCENUMPROC
 - imm/IMCENUMPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Imm.h
api_name:
 - EnumInputContext
---

## -description

An application-defined callback function that processes input contexts provided by the <a href="/windows/desktop/api/imm/nf-imm-immenuminputcontext">ImmEnumInputContext</a> function. The IMCENUMPROC type defines a pointer to this callback function. <b>EnumInputContext</b> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Handle to the input context.

### -param unnamedParam2

Application-supplied data.

## -returns

Returns a nonzero value to continue enumeration, or 0 to stop enumeration.

## -remarks

An application must register this function by passing its address to the <a href="/windows/desktop/api/imm/nf-imm-immenuminputcontext">ImmEnumInputContext</a> function.

## -see-also

<a href="/windows/desktop/api/imm/nf-imm-immenuminputcontext">ImmEnumInputContext</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
