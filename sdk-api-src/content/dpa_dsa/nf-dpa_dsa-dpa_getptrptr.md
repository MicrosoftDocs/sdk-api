---
UID: NF:dpa_dsa.DPA_GetPtrPtr
title: DPA_GetPtrPtr macro
author: windows-sdk-content
description: Gets the pointer to the internal pointer array of a dynamic pointer array (DPA).
old-location: controls\DPA_GetPtrPtr.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_getptrptr.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DPA_GetPtrPtr, DPA_GetPtrPtr macro [Windows Controls], _shell_DPA_GetPtrPtr, _shell_DPA_GetPtrPtr_cpp, controls.DPA_GetPtrPtr, controls._shell_DPA_GetPtrPtr, dpa_dsa/DPA_GetPtrPtr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: dpa_dsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dpa_dsa.h
api_name:
 - DPA_GetPtrPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DPA_GetPtrPtr macro


## -description


Gets the pointer to the internal pointer array of a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

A handle to an existing DPA.


## -remarks



Applications can use the return value to manipulate the contents of the DPA directly instead of using functions such as <a href="https://msdn.microsoft.com/3ba855f8-e077-4886-b2fc-002515242dd3">DPA_SetPtr</a>. The return value is invalidated by any operation that changes the number of elements in the DPA or destroys the DPA. For example, after calling function <a href="https://msdn.microsoft.com/275585f9-b26b-4528-a5b2-471dc1623a68">DPA_InsertPtr</a> on a DPA, any internal pointers retrieved by calling the macro <b>DPA_GetPtrPtr</b> on the same DPA are no longer valid.



