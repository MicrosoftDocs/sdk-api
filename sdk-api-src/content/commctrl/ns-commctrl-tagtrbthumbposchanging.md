---
UID: NS:commctrl.tagTRBTHUMBPOSCHANGING
title: tagTRBTHUMBPOSCHANGING
author: windows-sdk-content
description: Contains information about a trackbar change notification. This message is sent with the TRBN_THUMBPOSCHANGING notification.
old-location: controls\NMTRBTHUMBPOSCHANGING.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\trackbar\structures\nmtrbthumbposchanging.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: NMTRBTHUMBPOSCHANGING, NMTRBTHUMBPOSCHANGING structure [Windows Controls], _shell_NMTRBTHUMBPOSCHANGING, _shell_NMTRBTHUMBPOSCHANGING_cpp, commctrl/NMTRBTHUMBPOSCHANGING, controls.NMTRBTHUMBPOSCHANGING, controls._shell_NMTRBTHUMBPOSCHANGING, tagTRBTHUMBPOSCHANGING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - NMTRBTHUMBPOSCHANGING
product: Windows
targetos: Windows
req.typenames: NMTRBTHUMBPOSCHANGING
req.redist: 
---

# tagTRBTHUMBPOSCHANGING structure


## -description


Contains information about a trackbar change notification. This message is sent with the <a href="https://msdn.microsoft.com/0876e026-bc07-409d-b174-b97ed704fc11">TRBN_THUMBPOSCHANGING</a> notification.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

A <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that describes the notification.


### -field dwPos

Type: <b>DWORD</b>

Position on trackbar.


### -field nReason

Type: <b>int</b>

Type of movement as one of the following values: TB_LINEUP, TB_LINEDOWN, TB_PAGEUP, TB_PAGEDOWN, TB_THUMBPOSITION, TB_THUMBTRACK,
                TB_TOP, TB_BOTTOM, or TB_ENDTRACK.

