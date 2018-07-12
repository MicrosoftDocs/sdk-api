---
UID: NF:dpa_dsa.DSA_DeleteAllItems
title: DSA_DeleteAllItems function
author: windows-sdk-content
description: Deletes all items from a dynamic structure array (DSA).
old-location: controls\DSA_DeleteAllItems.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_deleteallitems.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: DSA_DeleteAllItems, DSA_DeleteAllItems function [Windows Controls], _shell_DSA_DeleteAllItems, _shell_DSA_DeleteAllItems_cpp, controls.DSA_DeleteAllItems, controls._shell_DSA_DeleteAllItems, dpa_dsa/DSA_DeleteAllItems
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_DeleteAllItems
product: Windows
targetos: Windows
req.lib: 
req.dll: Comctl32.dll
req.irql: 
---

# DSA_DeleteAllItems function


## -description


Deletes all items from a dynamic structure array (DSA).


## -parameters




### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the items were successfully deleted; otherwise, <b>FALSE</b>.



