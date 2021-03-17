---
UID: NF:wmcontainer.IMFASFStreamSelector.BitrateToStepNumber
title: IMFASFStreamSelector::BitrateToStepNumber (wmcontainer.h)
description: Retrieves the index of a bandwidth step that is appropriate for a specified bit rate. This method is used for multiple bit rate (MBR) content.
helpviewer_keywords: ["BitrateToStepNumber","BitrateToStepNumber method [Media Foundation]","BitrateToStepNumber method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","BitrateToStepNumber method","IMFASFStreamSelector.BitrateToStepNumber","IMFASFStreamSelector::BitrateToStepNumber","e2debbce-f6ee-45d7-bf05-2b07aa7719c7","mf.imfasfstreamselector_bitratetostepnumber","wmcontainer/IMFASFStreamSelector::BitrateToStepNumber"]
old-location: mf\imfasfstreamselector_bitratetostepnumber.htm
tech.root: mf
ms.assetid: e2debbce-f6ee-45d7-bf05-2b07aa7719c7
ms.date: 12/05/2018
ms.keywords: BitrateToStepNumber, BitrateToStepNumber method [Media Foundation], BitrateToStepNumber method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],BitrateToStepNumber method, IMFASFStreamSelector.BitrateToStepNumber, IMFASFStreamSelector::BitrateToStepNumber, e2debbce-f6ee-45d7-bf05-2b07aa7719c7, mf.imfasfstreamselector_bitratetostepnumber, wmcontainer/IMFASFStreamSelector::BitrateToStepNumber
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
 - IMFASFStreamSelector::BitrateToStepNumber
 - wmcontainer/IMFASFStreamSelector::BitrateToStepNumber
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
 - IMFASFStreamSelector.BitrateToStepNumber
---

# IMFASFStreamSelector::BitrateToStepNumber


## -description

Retrieves the index of a bandwidth step that is appropriate for a specified bit rate. This method is used for multiple bit rate (MBR) content.

## -parameters

### -param dwBitrate [in]

The bit rate to find a bandwidth step for.

### -param pdwStepNum [out]

Receives the step number. Use this number to retrieve information about the step by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getbandwidthstep">IMFASFStreamSelector::GetBandwidthStep</a>.

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

In a streaming multiple bit rate (MBR) scenario, call this method with the current data rate of the network connection to determine the correct step to use. You can also call this method periodically throughout streaming to ensure that the best step is used.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>