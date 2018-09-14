---
UID: NF:dpa_dsa.DPA_FastGetPtr
title: DPA_FastGetPtr macro
author: windows-sdk-content
description: Gets the value of the specified pointer in the dynamic pointer array (DPA).
old-location: controls\DPA_FastGetPtr.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\dpa_fastgetptr.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DPA_FastGetPtr, DPA_FastGetPtr macro [Windows Controls], _shell_DPA_FastGetPtr, _shell_DPA_FastGetPtr_cpp, controls.DPA_FastGetPtr, controls._shell_DPA_FastGetPtr, dpa_dsa/DPA_FastGetPtr
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
 - DPA_FastGetPtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DPA_FastGetPtr macro


## -description


Gets the value of the specified pointer in the dynamic pointer array (DPA).


## -parameters




### -param hdpa [in]

A handle to an existing DPA.


### -param i [in]

The index of the DPA item.


## -remarks



 Unlike function <a href="https://msdn.microsoft.com/1aca806d-4ab2-4286-a30f-66cd12000c44">DPA_GetPtr</a>, the macro <b>DPA_FastGetPtr</b> does no parameter validation. If the index specified in <b>DPA_FastGetPtr</b> is out of range, the behavior is undefined.



