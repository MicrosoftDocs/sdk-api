---
UID: NS:commctrl.NMCOMBOBOXEXA
title: NMCOMBOBOXEXA
author: windows-sdk-content
description: Contains information specific to ComboBoxEx items for use with notification codes.
old-location: controls\NMCOMBOBOXEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboex\structures\nmcomboboxex.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*PNMCOMBOBOXEXA, NMCOMBOBOXEX, NMCOMBOBOXEX structure [Windows Controls], NMCOMBOBOXEXA, NMCOMBOBOXEXW, PNMCOMBOBOXEX, PNMCOMBOBOXEX structure pointer [Windows Controls], _win32_NMCOMBOBOXEX, _win32_NMCOMBOBOXEX_cpp, commctrl/NMCOMBOBOXEX, commctrl/NMCOMBOBOXEXA, commctrl/NMCOMBOBOXEXW, commctrl/PNMCOMBOBOXEX, controls.NMCOMBOBOXEX, controls._win32_NMCOMBOBOXEX"
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
req.unicode-ansi: NMCOMBOBOXEXW (Unicode) and NMCOMBOBOXEXA (ANSI)
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
 - NMCOMBOBOXEX
 - NMCOMBOBOXEXA
 - NMCOMBOBOXEXW
product: Windows
targetos: Windows
req.typenames: NMCOMBOBOXEXA, *PNMCOMBOBOXEXA
req.redist: 
---

# NMCOMBOBOXEXA structure


## -description


Contains information specific to ComboBoxEx items for use with notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about the notification code. 


### -field ceItem

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775746(v=VS.85).aspx">COMBOBOXEXITEM</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Bb775746(v=VS.85).aspx">COMBOBOXEXITEM</a> structure that holds item information specific to the current notification. Upon receiving a notification code, the <b>COMBOBOXEXITEM</b> structure holds information required for the owner to respond. The members of this structure are often used as fields for the owner to return values in response to the notification. 

