---
UID: NS:commctrl.tagNMREBARCHEVRON
title: NMREBARCHEVRON (commctrl.h)
author: windows-sdk-content
description: Contains information used in handling the RBN_CHEVRONPUSHED notification code.
old-location: controls\NMREBARCHEVRON.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarchevron.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPNMREBARCHEVRON, LPNMREBARCHEVRON, LPNMREBARCHEVRON structure pointer [Windows Controls], NMREBARCHEVRON, NMREBARCHEVRON structure [Windows Controls], _win32_NMREBARCHEVRON, _win32_NMREBARCHEVRON_cpp, commctrl/LPNMREBARCHEVRON, commctrl/NMREBARCHEVRON, controls.NMREBARCHEVRON, controls._win32_NMREBARCHEVRON"
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
 - NMREBARCHEVRON
product: Windows
targetos: Windows
req.typenames: NMREBARCHEVRON, *LPNMREBARCHEVRON
req.redist: 
ms.custom: 19H1
---

# NMREBARCHEVRON structure


## -description


Contains information used in handling the <a href="https://msdn.microsoft.com/en-us/library/Bb774409(v=VS.85).aspx">RBN_CHEVRONPUSHED</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field uBand

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the band sending the notification. 


### -field wID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Application-defined identifier for the band. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined value associated with the band. 


### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that defines the area covered by the chevron. 


### -field lParamNM

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An application-defined value. If the <a href="https://msdn.microsoft.com/en-us/library/Bb774409(v=VS.85).aspx">RBN_CHEVRONPUSHED</a> notification was sent as a result of an <a href="https://msdn.microsoft.com/en-us/library/Bb774506(v=VS.85).aspx">RB_PUSHCHEVRON</a> message, this member contains the message's 
					<i>lAppValue</i> value. Otherwise, it is set to zero. 

