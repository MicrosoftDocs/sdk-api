---
UID: NS:commctrl.tagNMREBARAUTOBREAK
title: tagNMREBARAUTOBREAK
author: windows-sdk-content
description: Contains information used with the RBN_AUTOBREAK notification code.
old-location: controls\NMREBARAUTOBREAK.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarautobreak.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMREBARAUTOBREAK, LPNMREBARAUTOBREAK, LPNMREBARAUTOBREAK structure pointer [Windows Controls], NMREBARAUTOBREAK, NMREBARAUTOBREAK structure [Windows Controls], commctrl/LPNMREBARAUTOBREAK, commctrl/NMREBARAUTOBREAK, controls.NMREBARAUTOBREAK, controls.inet_NMREBARAUTOBREAK, inet_NMREBARAUTOBREAK, inet_NMREBARAUTOBREAK_cpp, tagNMREBARAUTOBREAK"
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
 - NMREBARAUTOBREAK
product: Windows
targetos: Windows
req.typenames: NMREBARAUTOBREAK, *LPNMREBARAUTOBREAK
req.redist: 
---

# tagNMREBARAUTOBREAK structure


## -description


Contains information used with the <a href="https://msdn.microsoft.com/b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864">RBN_AUTOBREAK</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that provides additional information about this notification code.


### -field uBand

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Zero-based index of the band affected by the notification. This is -1 if no band is affected.


### -field wID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Application-defined ID of the band.


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined value from the <b>lParam</b> member of the <a href="https://msdn.microsoft.com/67a59093-f387-47e2-b3bf-b12a7707da31">REBARBANDINFO</a> structure that defines the rebar band.


### -field uMsg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

ID of the message.


### -field fStyleCurrent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Style of the specified band.


### -field fAutoBreak

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>BOOL</b> that indicates whether a break should occur.

