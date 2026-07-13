---
UID: NS:digitalv.MCI_DGV_CAPTURE_PARMSW
title: MCI_DGV_CAPTURE_PARMSW (digitalv.h)
description: The MCI_DGV_CAPTURE_PARMSW (Unicode) structure (digitalv.h) contains parameters for the MCI_CAPTURE command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_CAPTURE_PARMSW","MCI_DGV_CAPTURE_PARMS","MCI_DGV_CAPTURE_PARMS structure [Windows Multimedia]","MCI_DGV_CAPTURE_PARMSW","_win32_MCI_DGV_CAPTURE_PARMS_str","digitalv/MCI_DGV_CAPTURE_PARMS","multimedia.mci_dgv_capture_parms"]
old-location: multimedia\mci_dgv_capture_parms.htm
tech.root: Multimedia
ms.assetid: 8ab62c4b-6db2-4a52-b015-a1d635e1edd4
ms.date: 08/16/2022
ms.keywords: '*LPMCI_DGV_CAPTURE_PARMSW, MCI_DGV_CAPTURE_PARMS, MCI_DGV_CAPTURE_PARMS structure [Windows Multimedia], MCI_DGV_CAPTURE_PARMSW, _win32_MCI_DGV_CAPTURE_PARMS_str, digitalv/MCI_DGV_CAPTURE_PARMS, multimedia.mci_dgv_capture_parms'
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
req.typenames: MCI_DGV_CAPTURE_PARMSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_CAPTURE_PARMSW
 - digitalv/MCI_DGV_CAPTURE_PARMSW
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
 - MCI_DGV_CAPTURE_PARMS
 - MCI_DGV_CAPTURE_PARMSW
---

# MCI_DGV_CAPTURE_PARMSW structure


## -description

The <b>MCI_DGV_CAPTURE_PARMS</b> structure contains parameters for the <a href="/windows/desktop/Multimedia/mci-capture">MCI_CAPTURE</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field lpstrFileName

Pointer to a null-terminated string specifying the destination path and filename for the file that receives the captured data.

### -field ptOffset

### -field ptExtent

### -field rc

Rectangle containing positioning information. <a href="/previous-versions//ms536136(v=vs.85)">RECT</a> structures are handled differently in MCI than in other parts of Windows; in MCI, <b>rc.right</b> contains the width of the rectangle and <b>rc.bottom</b> contains its height.

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <b>mciSendCommand</b> function to validate the members.





> [!NOTE]
> The digitalv.h header defines MCI_DGV_CAPTURE_PARMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/previous-versions//ms536136(v=vs.85)">RECT</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

