---
UID: NS:commctrl.tagNMREBARCHEVRON
title: tagNMREBARCHEVRON
author: windows-sdk-content
description: Contains information used in handling the RBN_CHEVRONPUSHED notification code.
old-location: controls\NMREBARCHEVRON.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebarchevron.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPNMREBARCHEVRON, LPNMREBARCHEVRON, LPNMREBARCHEVRON structure pointer [Windows Controls], NMREBARCHEVRON, NMREBARCHEVRON structure [Windows Controls], _win32_NMREBARCHEVRON, _win32_NMREBARCHEVRON_cpp, commctrl/LPNMREBARCHEVRON, commctrl/NMREBARCHEVRON, controls.NMREBARCHEVRON, controls._win32_NMREBARCHEVRON, tagNMREBARCHEVRON"
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
 - NMREBARCHEVRON
product: Windows
targetos: Windows
req.typenames: NMREBARCHEVRON, *LPNMREBARCHEVRON
req.redist: 
---

# tagNMREBARCHEVRON structure


## -description


Contains information used in handling the <a href="https://msdn.microsoft.com/58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84">RBN_CHEVRONPUSHED</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


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

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that defines the area covered by the chevron. 


### -field lParamNM

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

An application-defined value. If the <a href="https://msdn.microsoft.com/58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84">RBN_CHEVRONPUSHED</a> notification was sent as a result of an <a href="https://msdn.microsoft.com/00a8ce10-1fb2-488a-a6f9-1814f73f82bd">RB_PUSHCHEVRON</a> message, this member contains the message's 
					<i>lAppValue</i> value. Otherwise, it is set to zero. 

