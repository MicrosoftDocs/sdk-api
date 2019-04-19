---
UID: NF:dpa_dsa.DSA_Clone
title: DSA_Clone function (dpa_dsa.h)
author: windows-sdk-content
description: Duplicates a dynamic structure array (DSA).
old-location: controls\DSA_Clone.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_clone.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DSA_Clone, DSA_Clone function [Windows Controls], _shell_DSA_Clone, _shell_DSA_Clone_cpp, controls.DSA_Clone, controls._shell_DSA_Clone, dpa_dsa/DSA_Clone
ms.topic: function
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
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DSA_Clone function


## -description


Duplicates a dynamic structure array (DSA).


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


## -returns



Type: <b>HDSA</b>

Returns a handle to the clone, or <b>NULL</b> if the operation fails.




## -remarks



The clone consists of a copy of the structures stored in the original DSA. Subsequent changes to the original DSA do not affect the clone.



