---
UID: NS:shobjidl_core.PREVIEWHANDLERFRAMEINFO
title: PREVIEWHANDLERFRAMEINFO
author: windows-sdk-content
description: Accelerator table structure. Used by IPreviewHandlerFrame::GetWindowContext.
old-location: shell\PREVIEWHANDLERFRAMEINFO.htm
old-project: shell
ms.assetid: dd93675e-fd69-4fa3-a8e7-5238c27783d8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PREVIEWHANDLERFRAMEINFO, PREVIEWHANDLERFRAMEINFO structure [Windows Shell], _shell_PREVIEWHANDLERFRAMEINFO, shell.PREVIEWHANDLERFRAMEINFO, shobjidl_core/PREVIEWHANDLERFRAMEINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: PREVIEWHANDLERFRAMEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - PREVIEWHANDLERFRAMEINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# PREVIEWHANDLERFRAMEINFO structure


## -description


Accelerator table structure. Used by <a href="https://msdn.microsoft.com/953b7571-0da1-4e31-bb6f-1761f8103c6e">IPreviewHandlerFrame::GetWindowContext</a>.


## -struct-fields




### -field haccel

Type: <b>HACCEL</b>

A handle to the accelerator table.


### -field cAccelEntries

Type: <b>UINT</b>

The number of entries in the accelerator table.

