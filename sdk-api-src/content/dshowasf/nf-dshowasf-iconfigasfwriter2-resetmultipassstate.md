---
UID: NF:dshowasf.IConfigAsfWriter2.ResetMultiPassState
title: IConfigAsfWriter2::ResetMultiPassState (dshowasf.h)
description: The ResetMultiPassState method resets the filter when a preprocessing encoding pass is canceled before it is completed.
helpviewer_keywords: ["IConfigAsfWriter2 interface [DirectShow]","ResetMultiPassState method","IConfigAsfWriter2.ResetMultiPassState","IConfigAsfWriter2::ResetMultiPassState","IConfigAsfWriter2ResetMultiPassState","ResetMultiPassState","ResetMultiPassState method [DirectShow]","ResetMultiPassState method [DirectShow]","IConfigAsfWriter2 interface","dshow.iconfigasfwriter2_resetmultipassstate","dshowasf/IConfigAsfWriter2::ResetMultiPassState"]
old-location: dshow\iconfigasfwriter2_resetmultipassstate.htm
tech.root: dshow
ms.assetid: ca2ec239-ffb9-4030-9160-77a0c9be0a07
ms.date: 12/05/2018
ms.keywords: IConfigAsfWriter2 interface [DirectShow],ResetMultiPassState method, IConfigAsfWriter2.ResetMultiPassState, IConfigAsfWriter2::ResetMultiPassState, IConfigAsfWriter2ResetMultiPassState, ResetMultiPassState, ResetMultiPassState method [DirectShow], ResetMultiPassState method [DirectShow],IConfigAsfWriter2 interface, dshow.iconfigasfwriter2_resetmultipassstate, dshowasf/IConfigAsfWriter2::ResetMultiPassState
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigAsfWriter2::ResetMultiPassState
 - dshowasf/IConfigAsfWriter2::ResetMultiPassState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2.ResetMultiPassState
---

# IConfigAsfWriter2::ResetMultiPassState


## -description

The <code>ResetMultiPassState</code> method resets the filter when a preprocessing encoding pass is canceled before it is completed.

## -parameters

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
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter was not in a stopped state.

</td>
</tr>
</table>

## -remarks

This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an <a href="/windows/desktop/DirectShow/ec-preprocess-complete">EC_PREPROCESS_COMPLETE</a> event. It is not necessary to call this method if the preprocessing encoding pass completes without errors.

## -see-also

<a href="/windows/desktop/DirectShow/creating-asf-files-in-directshow">Creating ASF Files in DirectShow</a>



<a href="/windows/desktop/api/dshowasf/nn-dshowasf-iconfigasfwriter2">IConfigAsfWriter2 Interface</a>