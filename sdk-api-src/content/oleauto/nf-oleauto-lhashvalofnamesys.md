---
UID: NF:oleauto.LHashValOfNameSys
title: LHashValOfNameSys function (oleauto.h)
description: Computes a hash value for a name.
old-location: automat\lhashvalofnamesys.htm
tech.root: automat
ms.assetid: 929c2307-8e73-4576-a705-1cde1f728ba4
ms.date: 12/05/2018
ms.keywords: LHashValOfNameSys, LHashValOfNameSys function [Automation], _oa96_LHashValOfNameSys, automat.lhashvalofnamesys, oleauto/LHashValOfNameSys
f1_keywords:
- oleauto/LHashValOfNameSys
dev_langs:
- c++
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- LHashValOfNameSys
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LHashValOfNameSys function


## -description


Computes a hash value for a name.


## -parameters




### -param syskind

The SYSKIND of the target operating system.


### -param lcid

The LCID for the string.




### -param szName

The string whose hash value is to be computed.



## -returns



A hash value that represents the passed-in name.



