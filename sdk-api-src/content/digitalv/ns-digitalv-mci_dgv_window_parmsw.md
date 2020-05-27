---
UID: NS:digitalv.__unnamed_struct_35
title: MCI_DGV_WINDOW_PARMSW (digitalv.h)
description: The MCI_DGV_WINDOW_PARMS structure contains parameters for MCI_WINDOW command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_WINDOW_PARMSW","MCI_DGV_WINDOW_PARMS","MCI_DGV_WINDOW_PARMS structure [Windows Multimedia]","MCI_DGV_WINDOW_PARMSW","_win32_MCI_DGV_WINDOW_PARMS_str","digitalv/MCI_DGV_WINDOW_PARMS","multimedia.mci_dgv_window_parms"]
old-location: multimedia\mci_dgv_window_parms.htm
tech.root: Multimedia
ms.assetid: 89c16949-4501-4ca0-87b6-c5f2524879a7
ms.date: 12/05/2018
ms.keywords: '*LPMCI_DGV_WINDOW_PARMSW, MCI_DGV_WINDOW_PARMS, MCI_DGV_WINDOW_PARMS structure [Windows Multimedia], MCI_DGV_WINDOW_PARMSW, _win32_MCI_DGV_WINDOW_PARMS_str, digitalv/MCI_DGV_WINDOW_PARMS, multimedia.mci_dgv_window_parms'
f1_keywords:
- digitalv/MCI_DGV_WINDOW_PARMS
dev_langs:
- c++
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
- MCI_DGV_WINDOW_PARMS
- MCI_DGV_WINDOW_PARMSW
targetos: Windows
req.typenames: MCI_DGV_WINDOW_PARMSW
req.redist: 
ms.custom: 19H1
---

# MCI_DGV_WINDOW_PARMSW structure


## -description



The <b>MCI_DGV_WINDOW_PARMS</b> structure contains parameters for <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-window">MCI_WINDOW</a> command for digital-video devices.




## -struct-fields




### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.


### -field hWnd

Handle to the display window. If this member is MCI_DGV_WINDOW_HWND, the system uses a default window.


### -field wReserved1

 


### -field nCmdShow

Window-display command.


### -field wReserved2

 


### -field lpstrText

Window caption.


## -remarks



When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci">MCI</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-window">MCI_WINDOW</a>



<a href="https://docs.microsoft.com/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>
 

 

