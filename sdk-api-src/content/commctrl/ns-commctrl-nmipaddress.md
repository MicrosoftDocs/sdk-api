---
UID: NS:commctrl.tagNMIPADDRESS
title: NMIPADDRESS (commctrl.h)
description: Contains information for the IPN_FIELDCHANGED notification code.
helpviewer_keywords: ["*LPNMIPADDRESS","LPNMIPADDRESS","LPNMIPADDRESS structure pointer [Windows Controls]","NMIPADDRESS","NMIPADDRESS structure [Windows Controls]","_win32_NMIPADDRESS","_win32_NMIPADDRESS_cpp","commctrl/LPNMIPADDRESS","commctrl/NMIPADDRESS","controls.NMIPADDRESS","controls._win32_NMIPADDRESS"]
old-location: controls\NMIPADDRESS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\structures\nmipaddress.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMIPADDRESS, LPNMIPADDRESS, LPNMIPADDRESS structure pointer [Windows Controls], NMIPADDRESS, NMIPADDRESS structure [Windows Controls], _win32_NMIPADDRESS, _win32_NMIPADDRESS_cpp, commctrl/LPNMIPADDRESS, commctrl/NMIPADDRESS, controls.NMIPADDRESS, controls._win32_NMIPADDRESS'
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
targetos: Windows
req.typenames: NMIPADDRESS, *LPNMIPADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMIPADDRESS
 - commctrl/tagNMIPADDRESS
 - LPNMIPADDRESS
 - commctrl/LPNMIPADDRESS
 - NMIPADDRESS
 - commctrl/NMIPADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMIPADDRESS
---

# NMIPADDRESS structure


## -description

Contains information for the <a href="/windows/desktop/Controls/ipn-fieldchanged">IPN_FIELDCHANGED</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field iField

Type: <b>int</b>

The zero-based number of the field that was changed.

### -field iValue

Type: <b>int</b>

The new value of the field specified in the 
					<b>iField</b> member. While processing the <a href="/windows/desktop/Controls/ipn-fieldchanged">IPN_FIELDCHANGED</a> notification, this member can be set to any value that is within the range of the field and the control will place this new value in the field.