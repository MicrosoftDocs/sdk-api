---
UID: NS:digitalv.MCI_DGV_RESERVE_PARMSA
title: MCI_DGV_RESERVE_PARMSA (digitalv.h)
description: The MCI_DGV_RESERVE_PARMSA (ANSI) structure (digitalv.h) contains information for the MCI_RESERVE command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_RESERVE_PARMSA","MCI_DGV_RESERVE_PARMS","MCI_DGV_RESERVE_PARMS structure [Windows Multimedia]","MCI_DGV_RESERVE_PARMSA","_win32_MCI_DGV_RESERVE_PARMS_str","digitalv/MCI_DGV_RESERVE_PARMS","multimedia.mci_dgv_reserve_parms"]
old-location: multimedia\mci_dgv_reserve_parms.htm
tech.root: Multimedia
ms.assetid: f3105822-bdef-4e8d-912c-9d4b8d78cc47
ms.date: 08/16/2022
ms.keywords: '*LPMCI_DGV_RESERVE_PARMSA, MCI_DGV_RESERVE_PARMS, MCI_DGV_RESERVE_PARMS structure [Windows Multimedia], MCI_DGV_RESERVE_PARMSA, _win32_MCI_DGV_RESERVE_PARMS_str, digitalv/MCI_DGV_RESERVE_PARMS, multimedia.mci_dgv_reserve_parms'
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
req.typenames: MCI_DGV_RESERVE_PARMSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_RESERVE_PARMSA
 - digitalv/MCI_DGV_RESERVE_PARMSA
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
 - MCI_DGV_RESERVE_PARMS
 - MCI_DGV_RESERVE_PARMSA
---

# MCI_DGV_RESERVE_PARMSA structure


## -description

The <b>MCI_DGV_RESERVE_PARMS</b> structure contains information for the <a href="/windows/desktop/Multimedia/mci-reserve">MCI_RESERVE</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field lpstrPath

Pointer to a null-terminated string containing the location of a temporary file. The buffer contains only the drive and directory path of the file used to hold recorded data; the filename is specified by the device driver.

### -field dwSize

Size of reserved disk space.

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.





> [!NOTE]
> The digitalv.h header defines MCI_DGV_RESERVE_PARMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-reserve">MCI_RESERVE</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

