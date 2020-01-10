---
UID: NF:winnt.SUBLANGID
title: SUBLANGID macro (winnt.h)
description: Extracts a sublanguage identifier from a language identifier.
old-location: intl\sublangid.htm
tech.root: Intl
ms.assetid: 0441c915-f910-4ac7-ac0a-0b113f490d40
ms.date: 12/05/2018
ms.keywords: SUBLANGID, SUBLANGID macro [Internationalization for Windows Applications], _win32_SUBLANGID, intl.sublangid, winnt/SUBLANGID
f1_keywords:
- winnt/SUBLANGID
dev_langs:
- c++
req.header: winnt.h
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
- Winnt.h
api_name:
- SUBLANGID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SUBLANGID macro


## -description


Extracts a sublanguage identifier from a <a href="https://docs.microsoft.com/windows/desktop/Intl/language-identifiers">language identifier</a>.


## -parameters




### -param lgid

Language identifier. You can supply predefined values for this parameter, or create an identifier using the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="https://docs.microsoft.com/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nf-winnt-primarylangid">PRIMARYLANGID</a>
 

 

