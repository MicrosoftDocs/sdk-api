---
UID: NF:oleauto.LHashValOfName
title: LHashValOfName macro
author: windows-sdk-content
description: Computes a hash value for a name.
old-location: automat\lhashvalofname.htm
tech.root: automat
ms.assetid: 7cd401dc-95d0-4628-88f9-d00969228ea8
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: LHashValOfName, LHashValOfName function [Automation], _oa96_LHashValOfName, automat.lhashvalofname, oleauto/LHashValOfName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - LHashValOfName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This function is equivalent to <a href="https://msdn.microsoft.com/929c2307-8e73-4576-a705-1cde1f728ba4">LHashValOfNameSys</a>. The header file OleAuto.h contains macros that define <b>LHashValOfName</b> as <b>LHashValOfNameSys</b>, with the target operating system (syskind) based on the build preprocessor flags.

<b>LHashValOfName</b> computes a 32-bit hash value for a name that can be passed to <a href="https://msdn.microsoft.com/04814179-2555-4ba5-a08c-bff776c03ca3">ITypeComp::Bind</a>, <a href="https://msdn.microsoft.com/e1b6eb9c-aa5a-41b9-bc97-afa82206ccef">ITypeComp::BindType</a>, <a href="https://msdn.microsoft.com/932014a8-3a35-487a-b035-788fc28dacc2">ITypeLib::FindName</a>, or <a href="https://msdn.microsoft.com/c9cd5cc8-f65f-43de-9dd4-c617b56ecadf">ITypeLib::IsName</a>. The returned hash value is independent of the case of the characters in <i>szName</i>, as long as the language of the name is one of the languages supported by the OLE National Language Specification API. Any two strings that match when a case-insensitive comparison is done using any language produce the same hash value.




