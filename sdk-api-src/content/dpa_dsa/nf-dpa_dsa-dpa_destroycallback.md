---
UID: NF:dpa_dsa.DPA_DestroyCallback
title: DPA_DestroyCallback function
author: windows-sdk-content
description: Calls pfnCB on each element of the dynamic pointer array (DPA), then frees the DPA.
old-location: controls\DPA_DestroyCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_destroycallback.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DPA_DestroyCallback, DPA_DestroyCallback function [Windows Controls], _win32_DPA_DestroyCallback, _win32_DPA_DestroyCallback_cpp, controls.DPA_DestroyCallback, controls._win32_DPA_DestroyCallback, dpa_dsa/DPA_DestroyCallback
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
 - DPA_DestroyCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DPA_DestroyCallback function


## -description


<p class="CCE_Message">[<b>DPA_DestroyCallback</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Calls <i>pfnCB</i> on each element of the dynamic pointer array (DPA), then frees the DPA.


## -parameters




### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.


### -param pfnCB

Type: <b><a href="https://msdn.microsoft.com/7ee522bc-9a2c-417d-93d7-5f306fba511f">PFNDPAENUMCALLBACK</a></b>

A callback function pointer. See <a href="https://msdn.microsoft.com/7ee522bc-9a2c-417d-93d7-5f306fba511f">PFNDPAENUMCALLBACK</a> for the callback function prototype.


### -param pData

Type: <b>void*</b>

A callback data pointer. <i>pData</i> is passed as a parameter to <i>pfnCB</i>.


## -returns



No return value.



