---
UID: NF:wmcontainer.IMFASFStreamSelector.GetOutputMutex
title: IMFASFStreamSelector::GetOutputMutex (wmcontainer.h)
description: Retrieves a mutual exclusion object for an output.
helpviewer_keywords: ["GetOutputMutex","GetOutputMutex method [Media Foundation]","GetOutputMutex method [Media Foundation]","IMFASFStreamSelector interface","IMFASFStreamSelector interface [Media Foundation]","GetOutputMutex method","IMFASFStreamSelector.GetOutputMutex","IMFASFStreamSelector::GetOutputMutex","d134f4a9-9bca-454f-8dc1-2e152684a4bf","mf.imfasfstreamselector_getoutputmutex","wmcontainer/IMFASFStreamSelector::GetOutputMutex"]
old-location: mf\imfasfstreamselector_getoutputmutex.htm
tech.root: mf
ms.assetid: d134f4a9-9bca-454f-8dc1-2e152684a4bf
ms.date: 12/05/2018
ms.keywords: GetOutputMutex, GetOutputMutex method [Media Foundation], GetOutputMutex method [Media Foundation],IMFASFStreamSelector interface, IMFASFStreamSelector interface [Media Foundation],GetOutputMutex method, IMFASFStreamSelector.GetOutputMutex, IMFASFStreamSelector::GetOutputMutex, d134f4a9-9bca-454f-8dc1-2e152684a4bf, mf.imfasfstreamselector_getoutputmutex, wmcontainer/IMFASFStreamSelector::GetOutputMutex
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
 - IMFASFStreamSelector::GetOutputMutex
 - wmcontainer/IMFASFStreamSelector::GetOutputMutex
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
 - IMFASFStreamSelector.GetOutputMutex
---

# IMFASFStreamSelector::GetOutputMutex


## -description

Retrieves a mutual exclusion object for an output.

## -parameters

### -param dwOutputNum [in]

Output number for which to retrieve a mutual exclusion object.

### -param dwMutexNum [in]

Mutual exclusion number. This is an index of mutually exclusive relationships associated with the output. Set to a number between 0, and 1 less than the number of mutual exclusion objects retrieved by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputmutexcount">IMFASFStreamSelector::GetOutputMutexCount</a>.

### -param ppMutex [out]

Receives a pointer to the mutual exclusion object's <b>IUnknown</b> interface. The caller must release the interface.

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



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-getoutputmutexcount">IMFASFStreamSelector::GetOutputMutexCount</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamselector-setoutputmutexselection">IMFASFStreamSelector::SetOutputMutexSelection</a>