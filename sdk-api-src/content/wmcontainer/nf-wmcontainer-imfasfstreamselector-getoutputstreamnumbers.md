---
UID: NF:wmcontainer.IMFASFStreamSelector.GetOutputStreamNumbers
title: IMFASFStreamSelector::GetOutputStreamNumbers (wmcontainer.h)
description: Retrieves the stream numbers for all of the streams that are associated with an output.
helpviewer_keywords: ["4a999e7a-1b2e-4206-874a-ed93b868150b","GetOutputStreamNumbers","GetOutputStreamNumbers method [Media Foundation]","GetOutputStreamNumbers method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","GetOutputStreamNumbers method","IMFASFStreamSelector.GetOutputStreamNumbers","IMFASFStreamSelector::GetOutputStreamNumbers","mf.imfasfstreamselector_getoutputstreamnumbers","wmcontainer/IMFASFStreamSelector::GetOutputStreamNumbers"]
old-location: mf\imfasfstreamselector_getoutputstreamnumbers.htm
tech.root: mf
ms.assetid: 4a999e7a-1b2e-4206-874a-ed93b868150b
ms.date: 12/05/2018
ms.keywords: 4a999e7a-1b2e-4206-874a-ed93b868150b, GetOutputStreamNumbers, GetOutputStreamNumbers method [Media Foundation], GetOutputStreamNumbers method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetOutputStreamNumbers method, IMFASFStreamSelector.GetOutputStreamNumbers, IMFASFStreamSelector::GetOutputStreamNumbers, mf.imfasfstreamselector_getoutputstreamnumbers, wmcontainer/IMFASFStreamSelector::GetOutputStreamNumbers
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
 - IMFASFStreamSelector::GetOutputStreamNumbers
 - wmcontainer/IMFASFStreamSelector::GetOutputStreamNumbers
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
 - IMFASFStreamSelector.GetOutputStreamNumbers
---

# IMFASFStreamSelector::GetOutputStreamNumbers


## -description

Retrieves the stream numbers for all of the streams that are associated with an output.

## -parameters

### -param dwOutputNum [in]

The output number for which to retrieve stream numbers.

### -param rgwStreamNumbers [out]

Address of an array that receives the stream numbers associated with the output. The caller allocates the array. The array size must be at least as large as the value returned by the <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputstreamcount">IMFASFStreamSelector::GetOutputStreamCount</a> method.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid output number.

</td>
</tr>
</table>

## -remarks

An output is a stream in an ASF data section that will be parsed. If mutual exclusion is used, mutually exclusive streams share the same output.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector">IMFASFStreamSelector</a>