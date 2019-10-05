---
UID: NF:dpa_dsa.DPA_Create
title: DPA_Create function (dpa_dsa.h)
author: windows-sdk-content
description: Creates a dynamic pointer array (DPA).
old-location: controls\DPA_Create.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dpa_create.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DPA_Create, DPA_Create function [Windows Controls], _win32_DPA_Create, _win32_DPA_Create_cpp, controls.DPA_Create, controls._win32_DPA_Create, dpa_dsa/DPA_Create
ms.topic: function
f1_keywords: 
 - "dpa_dsa/DPA_Create"
dev_langs:
 - c++
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
 - DPA_Create
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DPA_Create function


## -description


<p class="CCE_Message">[<b>DPA_Create</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a dynamic pointer array (DPA).


## -parameters




### -param cItemGrow

Type: <b>int</b>

The number of elements by which the array should be expanded, if the DPA needs to be enlarged.


## -returns



Type: <b>HDPA</b>

Returns a handle to a DPA if successful, or <b>NULL</b> if the call fails.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_createex">DPA_CreateEx</a>
 

 

