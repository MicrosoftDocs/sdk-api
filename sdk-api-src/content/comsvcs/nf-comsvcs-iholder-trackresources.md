---
UID: NF:comsvcs.IHolder.TrackResourceS
title: IHolder::TrackResourceS (comsvcs.h)
description: Tracks the resource (string version).
helpviewer_keywords: ["IHolder interface [COM+]","TrackResourceS method","IHolder.TrackResourceS","IHolder::TrackResourceS","TrackResourceS","TrackResourceS method [COM+]","TrackResourceS method [COM+]","IHolder interface","_dtc_IHolder_TrackResourceS","comsvcs/IHolder::TrackResourceS","cos.iholder_trackresources"]
old-location: cos\iholder_trackresources.htm
tech.root: cos
ms.assetid: 1971820f-49aa-455d-a533-1a88fd8c28b8
ms.date: 12/05/2018
ms.keywords: IHolder interface [COM+],TrackResourceS method, IHolder.TrackResourceS, IHolder::TrackResourceS, TrackResourceS, TrackResourceS method [COM+], TrackResourceS method [COM+],IHolder interface, _dtc_IHolder_TrackResourceS, comsvcs/IHolder::TrackResourceS, cos.iholder_trackresources
req.header: comsvcs.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IHolder::TrackResourceS
 - comsvcs/IHolder::TrackResourceS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IHolder.TrackResourceS
---

# IHolder::TrackResourceS


## -description

Tracks the resource (string version).

## -parameters

### -param __MIDL__IHolder0004 [in]

The handle of the resource to be tracked. The Resource Dispenser has already created this resource before calling <b>TrackResourceS</b>.

## -returns

This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>SResId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed. The resource has not been tracked. The likely cause is that the caller's transaction is aborting.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a>