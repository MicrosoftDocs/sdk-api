---
UID: NS:digitalv.MCI_DGV_LIST_PARMSA
title: MCI_DGV_LIST_PARMSA (digitalv.h)
description: The MCI_DGV_LIST_PARMSA (ANSI) structure (digitalv.h) contains the information for the MCI_LIST command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_LIST_PARMSA","MCI_DGV_LIST_PARMS","MCI_DGV_LIST_PARMS structure [Windows Multimedia]","MCI_DGV_LIST_PARMSA","_win32_MCI_DGV_LIST_PARMS_str","digitalv/MCI_DGV_LIST_PARMS","multimedia.mci_dgv_list_parms"]
old-location: multimedia\mci_dgv_list_parms.htm
tech.root: Multimedia
ms.assetid: f1b44fca-6c33-4883-911c-7b18fc3084c2
ms.date: 08/16/2022
ms.keywords: '*LPMCI_DGV_LIST_PARMSA, MCI_DGV_LIST_PARMS, MCI_DGV_LIST_PARMS structure [Windows Multimedia], MCI_DGV_LIST_PARMSA, _win32_MCI_DGV_LIST_PARMS_str, digitalv/MCI_DGV_LIST_PARMS, multimedia.mci_dgv_list_parms'
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
req.typenames: MCI_DGV_LIST_PARMSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_LIST_PARMSA
 - digitalv/MCI_DGV_LIST_PARMSA
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
 - MCI_DGV_LIST_PARMS
 - MCI_DGV_LIST_PARMSA
---

# MCI_DGV_LIST_PARMSA structure


## -description

The <b>MCI_DGV_LIST_PARMS</b> structure contains the information for the <a href="/windows/desktop/Multimedia/mci-list">MCI_LIST</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field lpstrReturn

Buffer for return string.

### -field dwLength

Length, in bytes, of buffer.

### -field dwNumber

Index of item in list.

### -field dwItem

Type of list item.

### -field lpstrAlgorithm

String containing algorithm name.

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.





> [!NOTE]
> The digitalv.h header defines MCI_DGV_LIST_PARMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-list">MCI_LIST</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

