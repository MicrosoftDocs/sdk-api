---
UID: NS:digitalv.MCI_DGV_INFO_PARMSA
title: MCI_DGV_INFO_PARMSA (digitalv.h)
description: The MCI_DGV_INFO_PARMSA (ANSI) structure (digitalv.h) contains parameters for the MCI_INFO command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_INFO_PARMSA","MCI_DGV_INFO_PARMS","MCI_DGV_INFO_PARMS structure [Windows Multimedia]","MCI_DGV_INFO_PARMSA","_win32_MCI_DGV_INFO_PARMS_str","digitalv/MCI_DGV_INFO_PARMS","multimedia.mci_dgv_info_parms"]
old-location: multimedia\mci_dgv_info_parms.htm
tech.root: Multimedia
ms.assetid: 812a2445-d7a0-4751-8af5-7c9d5e673e27
ms.date: 08/16/2022
ms.keywords: '*LPMCI_DGV_INFO_PARMSA, MCI_DGV_INFO_PARMS, MCI_DGV_INFO_PARMS structure [Windows Multimedia], MCI_DGV_INFO_PARMSA, _win32_MCI_DGV_INFO_PARMS_str, digitalv/MCI_DGV_INFO_PARMS, multimedia.mci_dgv_info_parms'
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
req.typenames: MCI_DGV_INFO_PARMSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_INFO_PARMSA
 - digitalv/MCI_DGV_INFO_PARMSA
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
 - MCI_DGV_INFO_PARMS
 - MCI_DGV_INFO_PARMSA
---

# MCI_DGV_INFO_PARMSA structure


## -description

The <b>MCI_DGV_INFO_PARMS</b> structure contains parameters for the <a href="/windows/desktop/Multimedia/mci-info">MCI_INFO</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field lpstrReturn

Pointer to buffer for return string.

### -field dwRetSize

Size, in bytes, of return buffer.

### -field dwItem

Constant describing information to return.

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.





> [!NOTE]
> The digitalv.h header defines MCI_DGV_INFO_PARMS as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-info">MCI_INFO</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

