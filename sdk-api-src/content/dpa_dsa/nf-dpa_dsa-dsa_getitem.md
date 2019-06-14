---
UID: NF:dpa_dsa.DSA_GetItem
title: DSA_GetItem function (dpa_dsa.h)
author: windows-sdk-content
description: Gets an element from a dynamic structure array (DSA).
old-location: controls\DSA_GetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_getitem.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DSA_GetItem, DSA_GetItem function [Windows Controls], _win32_DSA_GetItem, _win32_DSA_GetItem_cpp, controls.DSA_GetItem, controls._win32_DSA_GetItem, dpa_dsa/DSA_GetItem
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
req.lib: 
req.dll: ComCtl32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComCtl32.dll
api_name:
 - DSA_GetItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DSA_GetItem function


## -description


Gets an element from a dynamic structure array (DSA).


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to the DSA containing the element.


### -param i [in]

Type: <b>int</b>

The index of the element to be retrieved (zero-based).


### -param pitem [out]

Type: <b>void*</b>

A pointer to a buffer which is filled with a copy of the specified element of the DSA.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



<b>DSA_GetItem</b> is not exported by name. To use it, you must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> and request ordinal 322 from ComCtl32.dll to obtain a function pointer.

Using the element pointer that this function retrieves, you can modify the data in that element directly. However, be aware that a subsequent insert or destroy operation could cause this pointer value to become invalid or to point to a different element.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitemptr">DSA_GetItemPtr</a>
 

 

