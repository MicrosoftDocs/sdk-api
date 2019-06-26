---
UID: NS:digitalv.__unnamed_struct_13
title: MCI_DGV_OPEN_PARMSW (digitalv.h)
author: windows-sdk-content
description: The MCI_DGV_OPEN_PARMS structure contains information for the MCI_OPEN command for digital-video devices.
old-location: multimedia\mci_dgv_open_parms.htm
tech.root: Multimedia
ms.assetid: 9256ab7f-1259-4c74-9766-fe3ed1c7215c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMCI_DGV_OPEN_PARMSW, MCI_DGV_OPEN_PARMS, MCI_DGV_OPEN_PARMS structure [Windows Multimedia], MCI_DGV_OPEN_PARMSW, _win32_MCI_DGV_OPEN_PARMS_str, digitalv/MCI_DGV_OPEN_PARMS, multimedia.mci_dgv_open_parms"
ms.topic: struct
f1_keywords: 
 - "digitalv/MCI_DGV_OPEN_PARMS"
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
 - MCI_DGV_OPEN_PARMS
product: Windows
targetos: Windows
req.typenames: MCI_DGV_OPEN_PARMSW
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_OPEN_PARMSW structure


## -description



The <b>MCI_DGV_OPEN_PARMS</b> structure contains information for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-open">MCI_OPEN</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field wDeviceID

Device ID returned to user.


### -field wReserved0

 


### -field lpstrDeviceType

Name or constant ID of device type.


### -field lpstrElementName

Optional device alias.


### -field lpstrAlias

Optional device alias.


### -field dwStyle

Window style.


### -field hWndParent

Handle to parent window.


### -field wReserved1

 




## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-open">MCI_OPEN</a>



<a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>
 

 

