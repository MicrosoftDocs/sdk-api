---
UID: NF:comsvcs.IHolder.RequestDestroyResource
title: IHolder::RequestDestroyResource (comsvcs.h)
description: Deletes a resource, calling its destructor to free memory and other associated system resources.
helpviewer_keywords: ["IHolder interface [COM+]","RequestDestroyResource method","IHolder.RequestDestroyResource","IHolder::RequestDestroyResource","RequestDestroyResource","RequestDestroyResource method [COM+]","RequestDestroyResource method [COM+]","IHolder interface","_dtc_IHolder_RequestDestroyResource","comsvcs/IHolder::RequestDestroyResource","cos.iholder_requestdestroyresource"]
old-location: cos\iholder_requestdestroyresource.htm
tech.root: cos
ms.assetid: c1602718-2221-4e49-a57c-f65f87174dc9
ms.date: 12/05/2018
ms.keywords: IHolder interface [COM+],RequestDestroyResource method, IHolder.RequestDestroyResource, IHolder::RequestDestroyResource, RequestDestroyResource, RequestDestroyResource method [COM+], RequestDestroyResource method [COM+],IHolder interface, _dtc_IHolder_RequestDestroyResource, comsvcs/IHolder::RequestDestroyResource, cos.iholder_requestdestroyresource
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
 - IHolder::RequestDestroyResource
 - comsvcs/IHolder::RequestDestroyResource
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
 - IHolder.RequestDestroyResource
---

# IHolder::RequestDestroyResource


## -description

Deletes a resource, calling its destructor to free memory and other associated system resources.

## -parameters

### -param __MIDL__IHolder0009 [in]

The resource to be destroyed.

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
<i>ResId</i> is not a valid resource handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL </b></dt>
</dl>
</td>
<td width="60%">
The method failed. The resource has not been destroyed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iholder">IHolder</a>