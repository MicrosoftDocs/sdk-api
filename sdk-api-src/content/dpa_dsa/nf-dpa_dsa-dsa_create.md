---
UID: NF:dpa_dsa.DSA_Create
title: DSA_Create function
author: windows-sdk-content
description: Creates a dynamic structure array (DSA).
old-location: controls\DSA_Create.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_create.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DSA_Create, DSA_Create function [Windows Controls], _win32_DSA_Create, _win32_DSA_Create_cpp, controls.DSA_Create, controls._win32_DSA_Create, dpa_dsa/DSA_Create
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
 - DSA_Create
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll
req.irql: 
---

# DSA_Create function


## -description


<p class="CCE_Message">[<b>DSA_Create</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Creates a dynamic structure array (DSA).


## -parameters




### -param cbItem [in]

Type: <b>int</b>

The size, in bytes, of the item.


### -param cItemGrow [in]

Type: <b>int</b>

The number of items by which the array should be incremented, if the DSA needs to be enlarged.


## -returns



Type: <b>HDSA</b>

Returns a handle to a DSA if successful, or <b>NULL</b> if the creation fails.




## -remarks



Unlike a dynamic pointer array (DPA), a DSA can contain elements of any size. This allows structures to be stored directly in the array.



