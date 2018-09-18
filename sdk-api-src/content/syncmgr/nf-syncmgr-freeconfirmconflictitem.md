---
UID: NF:syncmgr.FreeConfirmConflictItem
title: FreeConfirmConflictItem function
author: windows-sdk-content
description: Frees the resources that have been allocated for a CONFIRM_CONFLICT_ITEM structure.
old-location: shell\FreeConfirmConflictItem.htm
tech.root: shell
ms.assetid: 504a63e0-39e9-4228-ab3d-c34b272f8fd3
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: FreeConfirmConflictItem, FreeConfirmConflictItem function [Windows Shell], _shell_FreeConfirmConflictItem, shell.FreeConfirmConflictItem, syncmgr/FreeConfirmConflictItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: syncmgr.h
req.include-header: Syncmgr.idl
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
req.dll: None
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - FreeConfirmConflictItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FreeConfirmConflictItem function


## -description


Frees the resources that have been allocated for a <a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a> structure.


## -parameters




### -param pcci [in, out]

Type: <b><a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a> structure that stores pointers to the items for which memory is to be freed.


## -returns



This function does not return a value.



