---
UID: NF:commctrl.DateTime_GetIdealSize
title: DateTime_GetIdealSize macro
author: windows-sdk-content
description: Gets the size needed to display the control without clipping. Use this macro or send the DTM_GETIDEALSIZE message explicitly.
old-location: controls\DateTime_GetIdealSize.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getidealsize.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DateTime_GetIdealSize, DateTime_GetIdealSize macro [Windows Controls], _shell_DateTime_GetIdealSize, _shell_DateTime_GetIdealSize_cpp, commctrl/DateTime_GetIdealSize, controls.DateTime_GetIdealSize, controls._shell_DateTime_GetIdealSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	DateTime_GetIdealSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DateTime_GetIdealSize macro


## -description


Gets the size needed to display the control without clipping. Use this macro or send the <a href="https://msdn.microsoft.com/15ec26a1-645b-4a96-af66-1031e1a46c6c">DTM_GETIDEALSIZE</a> message explicitly.


## -parameters




### -param hdp [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the DTP control.


### -param psize [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a></b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure to receive the size. The caller is responsible for allocating this structure.

