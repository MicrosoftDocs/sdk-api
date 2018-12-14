---
UID: NS:commctrl.tagNMIPADDRESS
title: NMIPADDRESS
author: windows-sdk-content
description: Contains information for the IPN_FIELDCHANGED notification code.
old-location: controls\NMIPADDRESS.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\ipaddress\structures\nmipaddress.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMIPADDRESS, LPNMIPADDRESS, LPNMIPADDRESS structure pointer [Windows Controls], NMIPADDRESS, NMIPADDRESS structure [Windows Controls], _win32_NMIPADDRESS, _win32_NMIPADDRESS_cpp, commctrl/LPNMIPADDRESS, commctrl/NMIPADDRESS, controls.NMIPADDRESS, controls._win32_NMIPADDRESS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - NMIPADDRESS
product: Windows
targetos: Windows
req.typenames: NMIPADDRESS, *LPNMIPADDRESS
req.redist: 
---

# NMIPADDRESS structure


## -description


Contains information for the <a href="https://msdn.microsoft.com/en-us/library/Bb761376(v=VS.85).aspx">IPN_FIELDCHANGED</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

An <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field iField

Type: <b>int</b>

The zero-based number of the field that was changed. 


### -field iValue

Type: <b>int</b>

The new value of the field specified in the 
					<b>iField</b> member. While processing the <a href="https://msdn.microsoft.com/en-us/library/Bb761376(v=VS.85).aspx">IPN_FIELDCHANGED</a> notification, this member can be set to any value that is within the range of the field and the control will place this new value in the field. 

