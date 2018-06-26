---
UID: NE:shobjidl_core.FILE_USAGE_TYPE
title: FILE_USAGE_TYPE
author: windows-sdk-content
description: Constants used by IFileIsInUse::GetUsage to indicate how a file in use is being used.
old-location: shell\FILE_USAGE_TYPE.htm
old-project: shell
ms.assetid: 32b0e148-499a-401d-837c-8cea74cf9cac
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: FILE_USAGE_TYPE, FILE_USAGE_TYPE enumeration [Windows Shell], FUT_EDITING, FUT_GENERIC, FUT_PLAYING, _shell_FILE_USAGE_TYPE, shell.FILE_USAGE_TYPE, shobjidl_core/FILE_USAGE_TYPE, shobjidl_core/FUT_EDITING, shobjidl_core/FUT_GENERIC, shobjidl_core/FUT_PLAYING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILE_USAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - FILE_USAGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# FILE_USAGE_TYPE enumeration


## -description


Constants used by <a href="https://msdn.microsoft.com/7baba34d-b246-4d48-9f0c-e950d33ed5cf">IFileIsInUse::GetUsage</a> to indicate how a file in use is being used.


## -enum-fields




### -field FUT_PLAYING

The file is being played by the process that has it open.


### -field FUT_EDITING

The file is being edited by the process that has it open.


### -field FUT_GENERIC

The file is open in the process for an unspecified action or an action that does not readily fit into the other two categories.


## -remarks



The interpretation of "playing" or "editing" is left to the application's implementation of <a href="https://msdn.microsoft.com/68a4ab3d-165e-4917-8915-77f15901dbad">IFileIsInUse</a>. Generally, "playing" would refer to a media file while "editing" can refer to any file being altered in an application. However, the application itself best knows how to map these terms to its actions.



