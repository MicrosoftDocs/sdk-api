---
UID: NS:digitalv.MCI_DGV_OPEN_PARMSW
title: MCI_DGV_OPEN_PARMSW (digitalv.h)
description: The MCI_DGV_OPEN_PARMSW (Unicode) structure (digitalv.h) contains information for the MCI_OPEN command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_OPEN_PARMSW","MCI_DGV_OPEN_PARMS","MCI_DGV_OPEN_PARMS structure [Windows Multimedia]","MCI_DGV_OPEN_PARMSW","_win32_MCI_DGV_OPEN_PARMS_str","digitalv/MCI_DGV_OPEN_PARMS","multimedia.mci_dgv_open_parms"]
old-location: multimedia\mci_dgv_open_parms.htm
tech.root: Multimedia
ms.assetid: 9256ab7f-1259-4c74-9766-fe3ed1c7215c
ms.date: 08/16/2022
ms.keywords: '*LPMCI_DGV_OPEN_PARMSW, MCI_DGV_OPEN_PARMS, MCI_DGV_OPEN_PARMS structure [Windows Multimedia], MCI_DGV_OPEN_PARMSW, _win32_MCI_DGV_OPEN_PARMS_str, digitalv/MCI_DGV_OPEN_PARMS, multimedia.mci_dgv_open_parms'
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
targetos: Windows
req.typenames: MCI_DGV_OPEN_PARMSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_OPEN_PARMSW
 - digitalv/MCI_DGV_OPEN_PARMSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Digitalv.h
api_name:
 - MCI_DGV_OPEN_PARMS
 - MCI_DGV_OPEN_PARMSW
---

# MCI_DGV_OPEN_PARMSW structure


## -description

The <b>MCI_DGV_OPEN_PARMS</b> structure contains information for the <a href="/windows/desktop/Multimedia/mci-open">MCI_OPEN</a> command for digital-video devices.

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

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.





> [!NOTE]
> The digitalv.h header defines MCI_DGV_OPEN_PARMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-open">MCI_OPEN</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

