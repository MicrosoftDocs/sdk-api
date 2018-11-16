---
UID: NF:dpa_dsa.DPA_EnumCallback
title: DPA_EnumCallback function
author: windows-sdk-content
description: Iterates through the Dynamic Pointer Array (DPA) and calls pfnCB on each item.
old-location: controls\DPA_EnumCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_enumcallback.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DPA_EnumCallback, DPA_EnumCallback function [Windows Controls], _win32_DPA_EnumCallback, _win32_DPA_EnumCallback_cpp, controls.DPA_EnumCallback, controls._win32_DPA_EnumCallback, dpa_dsa/DPA_EnumCallback
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
 - DPA_EnumCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DPA_EnumCallback
: 
---

# DPA_EnumCallback function


## -description


<p class="CCE_Message">[<b>DPA_EnumCallback</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Iterates through the Dynamic Pointer Array (DPA) and calls <i>pfnCB</i> on each item. 


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




## -see-also




<a href="https://msdn.microsoft.com/2fe1546f-d517-4d63-a3a6-1d3ea0238b3d">PFNDAENUMCALLBACKCONST</a>
 

 

