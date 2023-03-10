---
UID: NS:mfapi._MFFOLDDOWN_MATRIX
title: MFFOLDDOWN_MATRIX (mfapi.h)
description: Contains coefficients used to transform multichannel audio into a smaller number of audio channels. This process is called fold-down.
helpviewer_keywords: ["59bf275d-583e-47aa-96ff-ce032c618081","MFFOLDDOWN_MATRIX","MFFOLDDOWN_MATRIX structure [Media Foundation]","mf.mffolddown_matrix","mfapi/MFFOLDDOWN_MATRIX"]
old-location: mf\mffolddown_matrix.htm
tech.root: mf
ms.assetid: 59bf275d-583e-47aa-96ff-ce032c618081
ms.date: 12/05/2018
ms.keywords: 59bf275d-583e-47aa-96ff-ce032c618081, MFFOLDDOWN_MATRIX, MFFOLDDOWN_MATRIX structure [Media Foundation], mf.mffolddown_matrix, mfapi/MFFOLDDOWN_MATRIX
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFFOLDDOWN_MATRIX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFFOLDDOWN_MATRIX
 - mfapi/_MFFOLDDOWN_MATRIX
 - MFFOLDDOWN_MATRIX
 - mfapi/MFFOLDDOWN_MATRIX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFFOLDDOWN_MATRIX
---

# MFFOLDDOWN_MATRIX structure


## -description

Contains coefficients used to transform multichannel audio into a smaller number of audio channels. This process is called <i>fold-down</i>.

## -struct-fields

### -field cbSize

Size of the structure, in bytes.

### -field cSrcChannels

Number of source channels.

### -field cDstChannels

Number of destination channels.

### -field dwChannelMask

Specifies the assignment of audio channels to speaker positions in the transformed audio. This member is a bitwise <b>OR</b> of flags that define the speaker positions. For a list of valid flags, see <a href="/windows/desktop/medfound/mf-mt-audio-channel-mask-attribute">MF_MT_AUDIO_CHANNEL_MASK</a> attribute.

### -field Coeff

Array that contains the fold-down coefficients. The number of coefficients is <b>cSrcChannels</b>×<b>cDstChannels</b>. If the number of coefficients is less than the size of the array, the remaining elements in the array are ignored. For more information about how the coefficients are applied, see <a href="/previous-versions/ms867218(v=msdn.10)">Windows Media Audio Professional Codec Features</a>.

## -remarks

To specify this information in the media type, set the <a href="/windows/desktop/medfound/mf-mt-audio-folddown-matrix-attribute">MF_MT_AUDIO_FOLDDOWN_MATRIX</a> attribute.

The ASF media source supports fold-down from six channels (5.1 audio) to two channels (stereo). It gets the information from the g_wszFold6To2Channels3 attribute in the ASF header. This attribute is documented in the Windows Media Format SDK documentation.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>