---
UID: NF:commctrl.DateTime_GetIdealSize
title: DateTime_GetIdealSize macro
author: windows-sdk-content
description: Gets the size needed to display the control without clipping. Use this macro or send the DTM_GETIDEALSIZE message explicitly.
old-location: controls\DateTime_GetIdealSize.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getidealsize.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DateTime_GetIdealSize, DateTime_GetIdealSize macro [Windows Controls], _shell_DateTime_GetIdealSize, _shell_DateTime_GetIdealSize_cpp, commctrl/DateTime_GetIdealSize, controls.DateTime_GetIdealSize, controls._shell_DateTime_GetIdealSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
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
 - Commctrl.h
api_name:
 - DateTime_GetIdealSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DateTime_GetIdealSize macro


## -description


Gets the size needed to display the control without clipping. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761757(v=VS.85).aspx">DTM_GETIDEALSIZE</a> message explicitly.


## -parameters




### -param hdp [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the DTP control.


### -param psize [out]

Type: <b><a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a></b>

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure to receive the size. The caller is responsible for allocating this structure.

