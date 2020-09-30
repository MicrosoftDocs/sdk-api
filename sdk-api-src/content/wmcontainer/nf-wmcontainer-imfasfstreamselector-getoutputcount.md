---
UID: NF:wmcontainer.IMFASFStreamSelector.GetOutputCount
title: IMFASFStreamSelector::GetOutputCount (wmcontainer.h)
description: Retrieves the number of outputs for the Advanced Systems Format (ASF) content.
helpviewer_keywords: ["09f00f52-f897-46f0-afb9-ae59913e04a1","GetOutputCount","GetOutputCount method [Media Foundation]","GetOutputCount method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","GetOutputCount method","IMFASFStreamSelector.GetOutputCount","IMFASFStreamSelector::GetOutputCount","mf.imfasfstreamselector_getoutputcount","wmcontainer/IMFASFStreamSelector::GetOutputCount"]
old-location: mf\imfasfstreamselector_getoutputcount.htm
tech.root: mf
ms.assetid: 09f00f52-f897-46f0-afb9-ae59913e04a1
ms.date: 12/05/2018
ms.keywords: 09f00f52-f897-46f0-afb9-ae59913e04a1, GetOutputCount, GetOutputCount method [Media Foundation], GetOutputCount method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetOutputCount method, IMFASFStreamSelector.GetOutputCount, IMFASFStreamSelector::GetOutputCount, mf.imfasfstreamselector_getoutputcount, wmcontainer/IMFASFStreamSelector::GetOutputCount
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
 - IMFASFStreamSelector::GetOutputCount
 - wmcontainer/IMFASFStreamSelector::GetOutputCount
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
 - IMFASFStreamSelector.GetOutputCount
---

# IMFASFStreamSelector::GetOutputCount


## -description

Retrieves the number of outputs for the Advanced Systems Format (ASF) content.

## -parameters

### -param pcOutputs [out]

Receives the number of outputs.

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

Outputs are streams in the ASF data section that will be parsed.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>