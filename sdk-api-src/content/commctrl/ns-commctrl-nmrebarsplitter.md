---
UID: NS:commctrl.tagNMREBARSPLITTER
title: NMREBARSPLITTER (commctrl.h)
description: Contains information used to handle an RBN_SPLITTERDRAG notification code.
helpviewer_keywords: ["*LPNMREBARSPLITTER","LPNMREBARSPLITTER","LPNMREBARSPLITTER structure pointer [Windows Controls]","NMREBARSPLITTER","NMREBARSPLITTER structure [Windows Controls]","_shell_NMREBARSPLITTER","_shell_NMREBARSPLITTER_cpp","commctrl/LPNMREBARSPLITTER","commctrl/NMREBARSPLITTER","controls.NMREBARSPLITTER","controls._shell_NMREBARSPLITTER"]
old-location: controls\NMREBARSPLITTER.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarsplitter.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMREBARSPLITTER, LPNMREBARSPLITTER, LPNMREBARSPLITTER structure pointer [Windows Controls], NMREBARSPLITTER, NMREBARSPLITTER structure [Windows Controls], _shell_NMREBARSPLITTER, _shell_NMREBARSPLITTER_cpp, commctrl/LPNMREBARSPLITTER, commctrl/NMREBARSPLITTER, controls.NMREBARSPLITTER, controls._shell_NMREBARSPLITTER'
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
targetos: Windows
req.typenames: NMREBARSPLITTER, *LPNMREBARSPLITTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMREBARSPLITTER
 - commctrl/tagNMREBARSPLITTER
 - LPNMREBARSPLITTER
 - commctrl/LPNMREBARSPLITTER
 - NMREBARSPLITTER
 - commctrl/NMREBARSPLITTER
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
 - NMREBARSPLITTER
---

# NMREBARSPLITTER structure


## -description

Contains information used to handle an <a href="/windows/desktop/Controls/rbn-splitterdrag">RBN_SPLITTERDRAG</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification.

### -field rcSizing

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

An <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that indicates the size the rebar will be after the drag operation completes.