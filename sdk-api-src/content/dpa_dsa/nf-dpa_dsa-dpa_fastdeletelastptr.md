---
UID: NF:dpa_dsa.DPA_FastDeleteLastPtr
title: DPA_FastDeleteLastPtr macro (dpa_dsa.h)
author: windows-sdk-content
description: Deletes the last pointer from a dynamic pointer array (DPA).
old-location: controls\DPA_FastDeleteLastPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_fastdeletelastptr.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DPA_FastDeleteLastPtr, DPA_FastDeleteLastPtr macro [Windows Controls], _shell_DPA_FastDeleteLastPtr, _shell_DPA_FastDeleteLastPtr_cpp, controls.DPA_FastDeleteLastPtr, controls._shell_DPA_FastDeleteLastPtr, dpa_dsa/DPA_FastDeleteLastPtr
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
 - DPA_FastDeleteLastPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DPA_FastDeleteLastPtr macro


## -description


Deletes the last pointer from a dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

A handle to an existing DPA.


## -remarks



If the DPA has no pointers, then the behavior is undefined.



