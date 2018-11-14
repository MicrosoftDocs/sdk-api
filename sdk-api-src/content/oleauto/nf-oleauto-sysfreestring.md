---
UID: NF:oleauto.SysFreeString
title: SysFreeString function
author: windows-sdk-content
description: Deallocates a string allocated previously by SysAllocString, SysAllocStringByteLen, SysReAllocString, SysAllocStringLen, or SysReAllocStringLen.
old-location: automat\sysfreestring.htm
tech.root: automat
ms.assetid: 8f230ee3-5f6e-4cb9-a910-9c90b754dcd3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SysFreeString, SysFreeString function [Automation], _oa96_SysFreeString, automat.sysfreestring, oleauto/SysFreeString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - SysFreeString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SysFreeString
: 
---

# SysFreeString function


## -description


Deallocates a string allocated previously by <a href="https://msdn.microsoft.com/9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>, <a href="https://msdn.microsoft.com/e7f49441-eff1-4c00-b61f-8522c4e250ef">SysAllocStringByteLen</a>, <a href="https://msdn.microsoft.com/0207c33b-c065-42bb-8d70-ccdc3fddb338">SysReAllocString</a>, <a href="https://msdn.microsoft.com/f98bff39-bc5f-4a81-85d7-d5228e20fbc8">SysAllocStringLen</a>, or <a href="https://msdn.microsoft.com/d134cff1-7cc8-4284-a216-3819615e3017">SysReAllocStringLen</a>.


## -parameters




### -param bstrString [in, optional]

The previously allocated string. If this parameter is <b>NULL</b>, the function simply returns.


## -returns



This function does not return a value.



