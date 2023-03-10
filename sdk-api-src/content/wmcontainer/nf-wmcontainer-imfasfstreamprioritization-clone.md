---
UID: NF:wmcontainer.IMFASFStreamPrioritization.Clone
title: IMFASFStreamPrioritization::Clone (wmcontainer.h)
description: Note  This interface is not implemented in this version of Media Foundation. Creates a copy of the ASF stream prioritization object.
helpviewer_keywords: ["Clone","Clone method [Media Foundation]","Clone method [Media Foundation]","IMFASFStreamPrioritization interface","IMFASFStreamPrioritization interface [Media Foundation]","Clone method","IMFASFStreamPrioritization.Clone","IMFASFStreamPrioritization::Clone","e4d7cc00-4483-4aa6-8f26-d25ddc5129bb","mf.imfasfstreamprioritization_clone","wmcontainer/IMFASFStreamPrioritization::Clone"]
old-location: mf\imfasfstreamprioritization_clone.htm
tech.root: mf
ms.assetid: e4d7cc00-4483-4aa6-8f26-d25ddc5129bb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Media Foundation], Clone method [Media Foundation],IMFASFStreamPrioritization interface, IMFASFStreamPrioritization interface [Media Foundation],Clone method, IMFASFStreamPrioritization.Clone, IMFASFStreamPrioritization::Clone, e4d7cc00-4483-4aa6-8f26-d25ddc5129bb, mf.imfasfstreamprioritization_clone, wmcontainer/IMFASFStreamPrioritization::Clone
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
 - IMFASFStreamPrioritization::Clone
 - wmcontainer/IMFASFStreamPrioritization::Clone
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
 - IMFASFStreamPrioritization.Clone
---

# IMFASFStreamPrioritization::Clone


## -description

<div class="alert"><b>Note</b>  This interface is not implemented in this version of Media Foundation.</div>
<div> </div>
Creates a copy of the ASF stream prioritization object.

## -parameters

### -param ppIStreamPrioritization [out]

Receives a pointer to the <a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization">IMFASFStreamPrioritization</a> interface of the new object. The caller must release the interface.

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

The new object is completely independent of the original.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization">IMFASFStreamPrioritization</a>