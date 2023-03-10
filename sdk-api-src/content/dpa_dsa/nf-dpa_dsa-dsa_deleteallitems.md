---
UID: NF:dpa_dsa.DSA_DeleteAllItems
title: DSA_DeleteAllItems function (dpa_dsa.h)
description: Deletes all items from a dynamic structure array (DSA).
helpviewer_keywords: ["DSA_DeleteAllItems","DSA_DeleteAllItems function [Windows Controls]","_shell_DSA_DeleteAllItems","_shell_DSA_DeleteAllItems_cpp","controls.DSA_DeleteAllItems","controls._shell_DSA_DeleteAllItems","dpa_dsa/DSA_DeleteAllItems"]
old-location: controls\DSA_DeleteAllItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\dsa_deleteallitems.htm
ms.date: 12/05/2018
ms.keywords: DSA_DeleteAllItems, DSA_DeleteAllItems function [Windows Controls], _shell_DSA_DeleteAllItems, _shell_DSA_DeleteAllItems_cpp, controls.DSA_DeleteAllItems, controls._shell_DSA_DeleteAllItems, dpa_dsa/DSA_DeleteAllItems
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DSA_DeleteAllItems
 - dpa_dsa/DSA_DeleteAllItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DSA_DeleteAllItems
req.apiset: ext-ms-win-shell-comctl32-da-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# DSA_DeleteAllItems function


## -description

Deletes all items from a dynamic structure array (DSA).

## -parameters

### -param hdsa [in]

Type: <b>HDSA</b>

A handle to an existing DSA.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the items were successfully deleted; otherwise, <b>FALSE</b>.
