---
UID: NS:commctrl.tagNMREBARAUTOBREAK
title: tagNMREBARAUTOBREAK
author: windows-sdk-content
description: Contains information used with the RBN_AUTOBREAK notification code.
old-location: controls\NMREBARAUTOBREAK.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarautobreak.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
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


Contains information used with the <a href="https://msdn.microsoft.com/en-us/library/Bb774403(v=VS.85).aspx">RBN_AUTOBREAK</a> notification code.


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that provides additional information about this notification code.


### -field uBand

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Zero-based index of the band affected by the notification. This is -1 if no band is affected.


### -field wID

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Application-defined ID of the band.


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPARAM</a></b>

Application-defined value from the <b>lParam</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Bb774393(v=VS.85).aspx">REBARBANDINFO</a> structure that defines the rebar band.


### -field uMsg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

ID of the message.


### -field fStyleCurrent

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Style of the specified band.


### -field fAutoBreak

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

<b>BOOL</b> that indicates whether a break should occur.

