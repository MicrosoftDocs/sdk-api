---
UID: NF:comsvcs.IHolder.UntrackResourceS
title: IHolder::UntrackResourceS (comsvcs.h)
description: Stops tracking a resource (string version).
helpviewer_keywords: ["IHolder interface [COM+]","UntrackResourceS method","IHolder.UntrackResourceS","IHolder::UntrackResourceS","UntrackResourceS","UntrackResourceS method [COM+]","UntrackResourceS method [COM+]","IHolder interface","_dtc_IHolder_UntrackResourceS","comsvcs/IHolder::UntrackResourceS","cos.iholder_untrackresources"]
old-location: cos\iholder_untrackresources.htm
tech.root: cos
ms.assetid: 03e54d2d-9dfb-46cf-abb9-d3f37784c449
ms.date: 12/05/2018
ms.keywords: IHolder interface [COM+],UntrackResourceS method, IHolder.UntrackResourceS, IHolder::UntrackResourceS, UntrackResourceS, UntrackResourceS method [COM+], UntrackResourceS method [COM+],IHolder interface, _dtc_IHolder_UntrackResourceS, comsvcs/IHolder::UntrackResourceS, cos.iholder_untrackresources
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
 - IHolder::UntrackResourceS
 - comsvcs/IHolder::UntrackResourceS
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
 - IHolder.UntrackResourceS
---

# IHolder::UntrackResourceS


## -description

Stops tracking a resource (string version).

## -parameters

### -param __MIDL__IHolder0007 [in]

The handle of the resource to stop tracking.

### -param __MIDL__IHolder0008 [in]

If <b>TRUE</b>, caller is requesting that the resource be destroyed, by calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-idispenserdriver-destroyresource">IDispenserDriver::DestroyResource</a>. If <b>FALSE</b>, caller destroys the resource.

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
The method failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispenserdriver">IDispenserDriver</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-idispensermanager">IDispenserManager</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a>