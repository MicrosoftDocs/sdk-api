---
UID: NF:dpa_dsa.DSA_GetItemPtr
title: DSA_GetItemPtr function
author: windows-sdk-content
description: Gets a pointer to an element from a dynamic structure array (DSA).
old-location: controls\DSA_GetItemPtr.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_getitemptr.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DSA_GetItemPtr, DSA_GetItemPtr function [Windows Controls], _win32_DSA_GetItemPtr, _win32_DSA_GetItemPtr_cpp, controls.DSA_GetItemPtr, controls._win32_DSA_GetItemPtr, dpa_dsa/DSA_GetItemPtr
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
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComCtl32.dll
api_name:
-	DSA_GetItemPtr
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll (version 4.0 or later)
req.irql: 
---

# DSA_GetItemPtr function


## -description


<p class="CCE_Message">[<b>DSA_GetItemPtr</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Gets a pointer to an element from a dynamic structure array (DSA).


## -parameters




### -param hdsa

TBD


### -param i

TBD




#### - index [in]

Type: <b>int</b>

The index of the element to be retrieved (zero-based).


#### - pdsa [in]

Type: <b>HDSA</b>

A handle to the DSA containing the element.


## -returns



Returns a pointer to the specified element or <b>NULL</b> if the call fails.




## -remarks



Using the element pointer that this function returns, you can modify the data in that element directly. However, be aware that a subsequent insert or destroy operation could cause this pointer value to become invalid or to point to a different element.



