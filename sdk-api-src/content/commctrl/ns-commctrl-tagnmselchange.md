---
UID: NS:commctrl.tagNMSELCHANGE
title: tagNMSELCHANGE
author: windows-sdk-content
description: Carries information required to process the MCN_SELCHANGE notification code.
old-location: controls\NMSELCHANGE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\structures\nmselchange.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPNMSELCHANGE, *LPNMSELECT, LPNMSELCHANGE, LPNMSELCHANGE structure pointer [Windows Controls], NMSELCHANGE, NMSELCHANGE structure [Windows Controls], NMSELECT, _win32_NMSELCHANGE, _win32_NMSELCHANGE_cpp, commctrl/LPNMSELCHANGE, commctrl/NMSELCHANGE, controls.NMSELCHANGE, controls._win32_NMSELCHANGE, tagNMSELCHANGE"
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
 - NMSELCHANGE
product: Windows
targetos: Windows
req.typenames: NMSELCHANGE, *LPNMSELCHANGE
req.redist: 
---

# tagNMSELCHANGE structure


## -description


Carries information required to process the <a href="https://msdn.microsoft.com/8923524f-d257-409d-bd3e-021684b88856">MCN_SELCHANGE</a> notification code. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about this notification. 


### -field stSelStart

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>


<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date for the first day in the user's selection range. 


### -field stSelEnd

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>


<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date for the last day in the user's selection range. 

