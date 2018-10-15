---
UID: NF:dpa_dsa.DSA_DestroyCallback
title: DSA_DestroyCallback function
author: windows-sdk-content
description: Iterates through a dynamic structure array (DSA), calling a specified callback function on each item. Upon reaching the end of the array, the DSA is freed.
old-location: controls\DSA_DestroyCallback.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_destroycallback.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DSA_DestroyCallback, DSA_DestroyCallback function [Windows Controls], _win32_DSA_DestroyCallback, _win32_DSA_DestroyCallback_cpp, controls.DSA_DestroyCallback, controls._win32_DSA_DestroyCallback, dpa_dsa/DSA_DestroyCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DSA_DestroyCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DSA_DestroyCallback function


## -description


<p class="CCE_Message">[<b>DSA_DestroyCallback</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Iterates through a dynamic structure array (DSA), calling a specified callback function on each item. Upon reaching the end of the array, the DSA is freed.


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to a DSA to walk and destroy.


### -param pfnCB [in]

Type: <b><a href="https://msdn.microsoft.com/2309ab9f-bf2e-413a-bf4f-b2782cd5af9e">PFNDSAENUMCALLBACK</a></b>

A callback function pointer. For the callback function prototype, see <a href="https://msdn.microsoft.com/2309ab9f-bf2e-413a-bf4f-b2782cd5af9e">PFNDSAENUMCALLBACK</a>.


### -param pData [in]

Type: <b>void*</b>

A callback data pointer. This pointer is, in turn, passed as a parameter to <i>pfnCB</i>.
        


## -returns



This function does not return a value.



