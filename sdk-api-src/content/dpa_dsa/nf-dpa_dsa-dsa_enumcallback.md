---
UID: NF:dpa_dsa.DSA_EnumCallback
title: DSA_EnumCallback function
author: windows-sdk-content
description: Iterates through the dynamic structure array (DSA) and calls pfnCB on each item.
old-location: controls\DSA_EnumCallback.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_enumcallback.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DSA_EnumCallback, DSA_EnumCallback function [Windows Controls], _shell_DSA_EnumCallback, _shell_DSA_EnumCallback_cpp, controls.DSA_EnumCallback, controls._shell_DSA_EnumCallback, dpa_dsa/DSA_EnumCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_EnumCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll
req.irql: 
---

# DSA_EnumCallback function


## -description


Iterates through the  dynamic structure array (DSA) and calls <i>pfnCB</i> on each item. 


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


### -param pfnCB [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb775711(v=VS.85).aspx">PFNDAENUMCALLBACK</a>*</b>

A callback function pointer. See <a href="https://msdn.microsoft.com/2309ab9f-bf2e-413a-bf4f-b2782cd5af9e">PFNDSAENUMCALLBACK</a> for the callback function prototype.


### -param pData [in]

Type: <b>void*</b>

A callback data pointer. <i>pData</i> is passed as a parameter to <i>pfnCB</i>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb775713(v=VS.85).aspx">PFNDAENUMCALLBACKCONST</a>
 

 

