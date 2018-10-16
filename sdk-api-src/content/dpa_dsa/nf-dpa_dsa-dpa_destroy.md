---
UID: NF:dpa_dsa.DPA_Destroy
title: DPA_Destroy function
author: windows-sdk-content
description: Frees a Dynamic Pointer Array (DPA).
old-location: controls\DPA_Destroy.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_destroy.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DPA_Destroy, DPA_Destroy function [Windows Controls], _win32_DPA_Destroy, _win32_DPA_Destroy_cpp, controls.DPA_Destroy, controls._win32_DPA_Destroy, dpa_dsa/DPA_Destroy
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
 - DPA_Destroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DPA_Destroy function


## -description


<p class="CCE_Message">[<b>DPA_Destroy</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Frees a Dynamic Pointer Array (DPA).


## -parameters




### -param hdpa

Type: <b>HDPA</b>

A handle to a DPA.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> on success, <b>FALSE</b> on failure.



