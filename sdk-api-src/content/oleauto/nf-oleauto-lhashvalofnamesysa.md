---
UID: NF:oleauto.LHashValOfNameSysA
title: LHashValOfNameSysA function (oleauto.h)
description: Computes a hash value for the specified name.
old-location: automat\lhashvalofnamesysa.htm
tech.root: automat
ms.assetid: 8a879533-c842-4ff7-b739-3f862281acaf
ms.date: 12/05/2018
ms.keywords: LHashValOfNameSysA, LHashValOfNameSysA function [Automation], _oa96_LHashValOfNameSysA, automat.lhashvalofnamesysa, oleauto/LHashValOfNameSysA
ms.topic: function
f1_keywords:
- oleauto/LHashValOfNameSysA
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
- LHashValOfNameSysA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LHashValOfNameSysA function


## -description


Computes a hash value for the specified name.


## -parameters




### -param syskind

The SYSKIND of the target operating system.




### -param lcid

The LCID for the string.




### -param szName

The string whose hash value is to be computed.



## -returns



A hash value that represents the specified name.




