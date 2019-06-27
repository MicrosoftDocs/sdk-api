---
UID: NS:digitalv.__unnamed_struct_31
title: MCI_DGV_STATUS_PARMSW (digitalv.h)
author: windows-sdk-content
description: The MCI_DGV_STATUS_PARMS structure contains parameters for the MCI_STATUS command for digital-video devices.
old-location: multimedia\mci_dgv_status_parms.htm
tech.root: Multimedia
ms.assetid: bbc09d4c-4231-48a8-97f6-54cbb32303b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMCI_DGV_STATUS_PARMSW, MCI_DGV_STATUS_PARMS, MCI_DGV_STATUS_PARMS structure [Windows Multimedia], MCI_DGV_STATUS_PARMSW, _win32_MCI_DGV_STATUS_PARMS_str, digitalv/MCI_DGV_STATUS_PARMS, multimedia.mci_dgv_status_parms"
ms.topic: struct
f1_keywords: 
 - "digitalv/MCI_DGV_STATUS_PARMS"
req.header: digitalv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Digitalv.h
api_name:
 - MCI_DGV_STATUS_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_STATUS_PARMSW
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_STATUS_PARMSW structure


## -description



The <b>MCI_DGV_STATUS_PARMS</b> structure contains parameters for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-status">MCI_STATUS</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field dwReturn

Buffer for return information.


### -field dwItem

Identifies capability being queried.


### -field dwTrack

Length or number of tracks.


### -field lpstrDrive

Specifies the approximate amount of disk space that can be obtained by the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-reserve">MCI_RESERVE</a> command.


### -field dwReference

Specifies the approximate location of the nearest previous intraframe-encoded image.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-reserve">MCI_RESERVE</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-status">MCI_STATUS</a>



<a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>
 

 

