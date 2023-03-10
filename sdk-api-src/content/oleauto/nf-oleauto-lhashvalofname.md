---
UID: NF:oleauto.LHashValOfName
title: LHashValOfName macro (oleauto.h)
description: Computes a hash value for a name. (LHashValOfName)
helpviewer_keywords: ["LHashValOfName","LHashValOfName function [Automation]","_oa96_LHashValOfName","automat.lhashvalofname","oleauto/LHashValOfName"]
old-location: automat\lhashvalofname.htm
tech.root: automat
ms.assetid: 7cd401dc-95d0-4628-88f9-d00969228ea8
ms.date: 12/05/2018
ms.keywords: LHashValOfName, LHashValOfName function [Automation], _oa96_LHashValOfName, automat.lhashvalofname, oleauto/LHashValOfName
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LHashValOfName
 - oleauto/LHashValOfName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - LHashValOfName
---

# LHashValOfName macro


## -description

Computes a hash value for a name.

## -parameters

### -param lcid

The LCID for the string.

### -param szName

The string whose hash value is to be computed.

## -remarks

This function is equivalent to <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-lhashvalofnamesys">LHashValOfNameSys</a>. The header file OleAuto.h contains macros that define <b>LHashValOfName</b> as <b>LHashValOfNameSys</b>, with the target operating system (syskind) based on the build preprocessor flags.

<b>LHashValOfName</b> computes a 32-bit hash value for a name that can be passed to <a href="/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bind">ITypeComp::Bind</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypecomp-bindtype">ITypeComp::BindType</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-findname">ITypeLib::FindName</a>, or <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-isname">ITypeLib::IsName</a>. The returned hash value is independent of the case of the characters in <i>szName</i>, as long as the language of the name is one of the languages supported by the OLE National Language Specification API. Any two strings that match when a case-insensitive comparison is done using any language produce the same hash value.
