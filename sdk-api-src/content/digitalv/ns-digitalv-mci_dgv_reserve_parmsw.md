---
UID: NS:digitalv.__unnamed_struct_19
title: MCI_DGV_RESERVE_PARMSW (digitalv.h)
author: windows-sdk-content
description: The MCI_DGV_RESERVE_PARMS structure contains information for the MCI_RESERVE command for digital-video devices.
old-location: multimedia\mci_dgv_reserve_parms.htm
tech.root: Multimedia
ms.assetid: f3105822-bdef-4e8d-912c-9d4b8d78cc47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMCI_DGV_RESERVE_PARMSW, MCI_DGV_RESERVE_PARMS, MCI_DGV_RESERVE_PARMS structure [Windows Multimedia], MCI_DGV_RESERVE_PARMSW, _win32_MCI_DGV_RESERVE_PARMS_str, digitalv/MCI_DGV_RESERVE_PARMS, multimedia.mci_dgv_reserve_parms"
ms.topic: struct
f1_keywords: 
 - "digitalv/MCI_DGV_RESERVE_PARMS"
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
 - MCI_DGV_RESERVE_PARMS
 - MCI_DGV_RESERVE_PARMSW
targetos: Windows
req.typenames: MCI_DGV_RESERVE_PARMSW
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_RESERVE_PARMSW structure


## -description



The <b>MCI_DGV_RESERVE_PARMS</b> structure contains information for the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-reserve">MCI_RESERVE</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field lpstrPath

Pointer to a null-terminated string containing the location of a temporary file. The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.


### -field dwSize

Size of reserved disk space.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-reserve">MCI_RESERVE</a>



<a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>
 

 

