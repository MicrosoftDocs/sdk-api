---
UID: NF:dpa_dsa.DPA_Create
title: DPA_Create function
author: windows-sdk-content
description: Creates a dynamic pointer array (DPA).
old-location: controls\DPA_Create.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_create.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: DPA_Create, DPA_Create function [Windows Controls], _win32_DPA_Create, _win32_DPA_Create_cpp, controls.DPA_Create, controls._win32_DPA_Create, dpa_dsa/DPA_Create
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DPA_Create
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
---

# DPA_Create function


## -description


<p class="CCE_Message">[<b>DPA_Create</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a dynamic pointer array (DPA).


## -parameters




### -param cItemGrow

TBD




#### - cpGrow

Type: <b>int</b>

The number of elements by which the array should be expanded, if the DPA needs to be enlarged.


## -returns



Type: <b>HDPA</b>

Returns a handle to a DPA if successful, or <b>NULL</b> if the call fails.




## -see-also




<a href="https://msdn.microsoft.com/a77ad74e-3bb5-414a-9cd7-db4b1c6e8116">DPA_CreateEx</a>
 

 

