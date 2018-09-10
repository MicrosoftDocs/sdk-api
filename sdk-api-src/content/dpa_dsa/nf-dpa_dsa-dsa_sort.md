---
UID: NF:dpa_dsa.DSA_Sort
title: DSA_Sort function
author: windows-sdk-content
description: Sorts the items in a dynamic structure array (DSA).
old-location: controls\DSA_Sort.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_sort.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DSA_Sort, DSA_Sort function [Windows Controls], _shell_DSA_Sort, _shell_DSA_Sort_cpp, controls.DSA_Sort, controls._shell_DSA_Sort, dpa_dsa/DSA_Sort
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DSA_Sort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DSA_Sort function


## -description


Sorts the items in a dynamic structure array (DSA).


## -parameters




### -param pdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


### -param pfnCompare [in]

Type: <b><a href="https://msdn.microsoft.com/be3c1ebd-4e22-42a5-afea-bd1bb9a86ed1">PFNDACOMPARE</a></b>

A comparison function pointer. See <a href="https://msdn.microsoft.com/b2b03db5-e595-4778-b51a-0087d663b026">PFNDPACOMPARE</a> for the comparison function prototype.


### -param lParam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An additional parameter to be passed to <i>pfnCmp</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> on success or <b>FALSE</b> on failure.



