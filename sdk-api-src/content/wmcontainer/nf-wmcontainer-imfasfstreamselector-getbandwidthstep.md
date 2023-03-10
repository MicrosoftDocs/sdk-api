---
UID: NF:wmcontainer.IMFASFStreamSelector.GetBandwidthStep
title: IMFASFStreamSelector::GetBandwidthStep (wmcontainer.h)
description: Retrieves the stream numbers that apply to a bandwidth step. This method is used for multiple bit rate (MBR) content.
helpviewer_keywords: ["82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c","GetBandwidthStep","GetBandwidthStep method [Media Foundation]","GetBandwidthStep method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","GetBandwidthStep method","IMFASFStreamSelector.GetBandwidthStep","IMFASFStreamSelector::GetBandwidthStep","mf.imfasfstreamselector_getbandwidthstep","wmcontainer/IMFASFStreamSelector::GetBandwidthStep"]
old-location: mf\imfasfstreamselector_getbandwidthstep.htm
tech.root: mf
ms.assetid: 82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c
ms.date: 12/05/2018
ms.keywords: 82d9b642-48e3-4ef5-b0e1-b72f1dd39b2c, GetBandwidthStep, GetBandwidthStep method [Media Foundation], GetBandwidthStep method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetBandwidthStep method, IMFASFStreamSelector.GetBandwidthStep, IMFASFStreamSelector::GetBandwidthStep, mf.imfasfstreamselector_getbandwidthstep, wmcontainer/IMFASFStreamSelector::GetBandwidthStep
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFStreamSelector::GetBandwidthStep
 - wmcontainer/IMFASFStreamSelector::GetBandwidthStep
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamSelector.GetBandwidthStep
---

# IMFASFStreamSelector::GetBandwidthStep


## -description

Retrieves the stream numbers that apply to a bandwidth step. This method is used for multiple bit rate (MBR) content.

## -parameters

### -param dwStepNum [in]

Bandwidth step number for which to retrieve information. Set this value to a number between 0, and 1 less than the number of bandwidth steps returned by <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstepcount">IMFASFStreamSelector::GetBandwidthStepCount</a>.

### -param pdwBitrate [out]

Receives the bit rate associated with the bandwidth step.

### -param rgwStreamNumbers [out]

Address of an array that receives the stream numbers. The caller allocates the array. The array size must be at least as large as the value returned by the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getstreamcount">IMFASFStreamSelector::GetStreamCount</a> method.

### -param rgSelections [out]

Address of an array that receives the selection status of each stream, as an <a href="/windows/desktop/api/wmcontainer/ne-wmcontainer-asf_selection_status">ASF_SELECTION_STATUS</a> value. The members of this array correspond to the members of the <i>rgwStreamNumbers</i> array by index. The caller allocates the array. The array size must be at least as large as the value returned by the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getstreamcount">IMFASFStreamSelector::GetStreamCount</a> method.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Bandwidth steps are bandwidth levels used for MBR content. If you stream MBR content, you can choose the bandwidth step that matches the network conditions to avoid interruptions during playback.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstepcount">IMFASFStreamSelector::GetBandwidthStepCount</a>