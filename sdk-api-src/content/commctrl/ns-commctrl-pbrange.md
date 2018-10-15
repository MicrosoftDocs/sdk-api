---
UID: NS:commctrl.PBRANGE
title: PBRANGE
author: windows-sdk-content
description: Contains information about the high and low limits of a progress bar control. This structure is used with the PBM_GETRANGE message.
old-location: controls\PBRANGE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\progbar\structures\pbrange.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PPBRANGE, PBRANGE, PBRANGE structure [Windows Controls], PPBRANGE, PPBRANGE structure pointer [Windows Controls], _win32_PBRANGE, _win32_PBRANGE_cpp, commctrl/PBRANGE, commctrl/PPBRANGE, controls.PBRANGE, controls._win32_PBRANGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - PBRANGE
product: Windows
targetos: Windows
req.typenames: PBRANGE, *PPBRANGE
req.redist: 
---

# PBRANGE structure


## -description


Contains information about the high and low limits of a progress bar control. This structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Bb760832(v=VS.85).aspx">PBM_GETRANGE</a> message. 


## -struct-fields




### -field iLow

Type: <b>int</b>

Low limit for the progress bar control. This is a signed integer. 


### -field iHigh

Type: <b>int</b>

High limit for the progress bar control. This is a signed integer. 

