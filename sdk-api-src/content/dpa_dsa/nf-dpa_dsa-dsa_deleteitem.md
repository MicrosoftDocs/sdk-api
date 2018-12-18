---
UID: NF:dpa_dsa.DSA_DeleteItem
title: DSA_DeleteItem function
author: windows-sdk-content
description: Deletes an item from a dynamic structure array (DSA).
old-location: controls\DSA_DeleteItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_deleteitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DSA_DeleteItem, DSA_DeleteItem function [Windows Controls], _shell_DSA_DeleteItem, _shell_DSA_DeleteItem_cpp, controls.DSA_DeleteItem, controls._shell_DSA_DeleteItem, dpa_dsa/DSA_DeleteItem
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
req.dll: Comctl32.dll (version 4.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_DeleteItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DSA_DeleteItem function


## -description


<p class="CCE_Message">[<b>DSA_DeleteItem</b> is available through Windows XP with Service Pack 2 (SP2). It might be altered or unavailable in subsequent versions.]

Deletes an item from a dynamic structure array (DSA).


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


### -param i [in]

Type: <b>int</b>

The zero-based index of the item to delete.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the item was successfully deleted; otherwise, <b>FALSE</b>.




## -remarks



<b>DSA_DeleteItem</b> is not exported by name. To use it, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> and request ordinal 326 from ComCtl32.dll to obtain a function pointer.



