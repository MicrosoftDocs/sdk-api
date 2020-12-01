---
UID: NF:winbase.MAKEINTATOM
title: MAKEINTATOM macro (winbase.h)
description: Converts the specified atom into a string, so it can be passed to functions which accept either atoms or strings.
helpviewer_keywords: ["MAKEINTATOM","MAKEINTATOM macro [Data Exchange]","_win32_MAKEINTATOM","_win32_makeintatom_cpp","dataxchg.makeintatom","winbase/MAKEINTATOM","winui._win32_makeintatom"]
old-location: dataxchg\makeintatom.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\atoms\atomreference\atommacros\makeintatom.htm
ms.date: 12/05/2018
ms.keywords: MAKEINTATOM, MAKEINTATOM macro [Data Exchange], _win32_MAKEINTATOM, _win32_makeintatom_cpp, dataxchg.makeintatom, winbase/MAKEINTATOM, winui._win32_makeintatom
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAKEINTATOM
 - winbase/MAKEINTATOM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbase.h
api_name:
 - MAKEINTATOM
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

<a href="/windows/desktop/api/winbase/nf-winbase-addatomw">AddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-deleteatom">DeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getatomnamea">GetAtomName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globaldeleteatom">GlobalDeleteAtom</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalgetatomnamea">GlobalGetAtomName</a>



<b>Reference</b>