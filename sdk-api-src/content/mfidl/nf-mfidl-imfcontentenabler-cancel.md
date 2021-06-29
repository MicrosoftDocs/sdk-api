---
UID: NF:mfidl.IMFContentEnabler.Cancel
title: IMFContentEnabler::Cancel (mfidl.h)
description: Cancels a pending content enabling action.
helpviewer_keywords: ["Cancel","Cancel method [Media Foundation]","Cancel method [Media Foundation]","IMFContentEnabler interface","IMFContentEnabler interface [Media Foundation]","Cancel method","IMFContentEnabler.Cancel","IMFContentEnabler::Cancel","e273b702-1f42-4aeb-9259-778d3f206682","mf.imfcontentenabler_cancel","mfidl/IMFContentEnabler::Cancel"]
old-location: mf\imfcontentenabler_cancel.htm
tech.root: mf
ms.assetid: e273b702-1f42-4aeb-9259-778d3f206682
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Media Foundation], Cancel method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],Cancel method, IMFContentEnabler.Cancel, IMFContentEnabler::Cancel, e273b702-1f42-4aeb-9259-778d3f206682, mf.imfcontentenabler_cancel, mfidl/IMFContentEnabler::Cancel
req.header: mfidl.h
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFContentEnabler::Cancel
 - mfidl/IMFContentEnabler::Cancel
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
 - IMFContentEnabler.Cancel
---

# IMFContentEnabler::Cancel


## -description

Cancels a pending content enabling action.



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

The content enabler sends an <a href="/windows/desktop/medfound/meenablercompleted">MEEnablerCompleted</a> event with a status code of E_CANCEL.

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a>
