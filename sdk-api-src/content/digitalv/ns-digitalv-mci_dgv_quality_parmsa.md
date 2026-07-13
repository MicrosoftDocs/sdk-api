---
UID: NS:digitalv.MCI_DGV_QUALITY_PARMSA
title: MCI_DGV_QUALITY_PARMSA (digitalv.h)
description: The MCI_DGV_QUALITY_PARMSA (ANSI) structure (digitalv.h) contains parameters for the MCI_QUALITY command for digital-video devices.
helpviewer_keywords: ["*LPMCI_DGV_QUALITY_PARMSA","MCI_DGV_QUALITY_PARMS","MCI_DGV_QUALITY_PARMS structure [Windows Multimedia]","MCI_DGV_QUALITY_PARMSA","MCI_QUALITY_ITEM_AUDIO","MCI_QUALITY_ITEM_STILL","MCI_QUALITY_ITEM_VIDEO","_win32_MCI_DGV_QUALITY_PARMS_str","digitalv/MCI_DGV_QUALITY_PARMS","multimedia.mci_dgv_quality_parms"]
old-location: multimedia\mci_dgv_quality_parms.htm
tech.root: Multimedia
ms.assetid: 0a150c37-9699-4b9e-b539-bdeb980b2f28
ms.date: 08/16/2022
ms.keywords: '*LPMCI_DGV_QUALITY_PARMSA, MCI_DGV_QUALITY_PARMS, MCI_DGV_QUALITY_PARMS structure [Windows Multimedia], MCI_DGV_QUALITY_PARMSA, MCI_QUALITY_ITEM_AUDIO, MCI_QUALITY_ITEM_STILL, MCI_QUALITY_ITEM_VIDEO, _win32_MCI_DGV_QUALITY_PARMS_str, digitalv/MCI_DGV_QUALITY_PARMS, multimedia.mci_dgv_quality_parms'
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
req.typenames: MCI_DGV_QUALITY_PARMSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCI_DGV_QUALITY_PARMSA
 - digitalv/MCI_DGV_QUALITY_PARMSA
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
 - MCI_DGV_QUALITY_PARMS
 - MCI_DGV_QUALITY_PARMSA
---

# MCI_DGV_QUALITY_PARMSA structure


## -description

The <b>MCI_DGV_QUALITY_PARMS</b> structure contains parameters for the <a href="/windows/desktop/Multimedia/mci-quality">MCI_QUALITY</a> command for digital-video devices.

## -struct-fields

### -field dwCallback

The low-order word specifies a window handle used for the MCI_NOTIFY flag.

### -field dwItem

One of the following constants indicating the type of algorithm:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="MCI_QUALITY_ITEM_AUDIO"></a><a id="mci_quality_item_audio"></a><dl>
<dt><b>MCI_QUALITY_ITEM_AUDIO</b></dt>
</dl>
</td>
<td width="60%">
Definitions are for an audio compression algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_QUALITY_ITEM_STILL"></a><a id="mci_quality_item_still"></a><dl>
<dt><b>MCI_QUALITY_ITEM_STILL</b></dt>
</dl>
</td>
<td width="60%">
Definitions are for a still video compression algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="MCI_QUALITY_ITEM_VIDEO"></a><a id="mci_quality_item_video"></a><dl>
<dt><b>MCI_QUALITY_ITEM_VIDEO</b></dt>
</dl>
</td>
<td width="60%">
Definitions are for a video compression algorithm.

</td>
</tr>
</table>

### -field lpstrName

String naming description.

### -field lpstrAlgorithm

String naming algorithm.

### -field dwHandle

Handle to a structure containing information describing the quality attributes.

## -remarks

When assigning data to the members of this structure, set the corresponding flags in the <i>fdwCommand</i> parameter of the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function to validate the members.





> [!NOTE]
> The digitalv.h header defines MCI_DGV_QUALITY_PARMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/mci">MCI</a>



<a href="/windows/desktop/Multimedia/mci-structures">MCI Structures</a>



<a href="/windows/desktop/Multimedia/mci-quality">MCI_QUALITY</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

