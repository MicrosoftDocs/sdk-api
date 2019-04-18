---
UID: NN:directml.IDMLObject
title: IDMLObject
author: windows-sdk-content
description: An interface from which IDMLDevice and IDMLDeviceChild inherit directly (and all other interfaces, indirectly).
old-location: direct3d12\idmlobject.htm
tech.root: direct3d12
ms.assetid: E41D99AF-838B-43D3-AD3F-A2F7CA85C714
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLObject, IDMLObject interface, IDMLObject interface,described, direct3d12.idmlobject, directml/IDMLObject
ms.topic: interface
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLObject interface


## -description






An interface from which [IDMLDevice](/windows/desktop/api/directml/nn-directml-idmldevice) and [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) inherit directly (and all other interfaces, indirectly). Consequently, it provides methods common to all DirectML interfaces, specifically methods to associate private data, and to annotate object names.


## -inheritance

The <b>IDMLObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDMLObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDMLObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmlobject-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Gets application-defined data from a DirectML device object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmlobject-setname">SetName</a>
</td>
<td align="left" width="63%">
Associates a name with the DirectML device object.
          This name is for use in debug diagnostics and tools.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmlobject-setprivatedata">SetPrivateData</a>
</td>
<td align="left" width="63%">
Sets application-defined data to a DirectML device object, and associates that data with an application-defined <b>GUID</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/directml/nf-directml-idmlobject-setprivatedatainterface">SetPrivateDataInterface</a>
</td>
<td align="left" width="63%">
Associates an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-derived interface with the DirectML device object, and associates that interface with an application-defined <b>GUID</b>.

</td>
</tr>
</table> 

