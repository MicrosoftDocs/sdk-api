---
UID: NN:vdshwprv.IVdsAsync
title: IVdsAsync (vdshwprv.h)
author: windows-sdk-content
description: Manages asynchronous operations. Methods that initiate asynchronous operations return a pointer to an IVdsAsync interface, allowing the caller to optionally cancel, wait for, or query the status of the asynchronous operation.
old-location: base\ivdsasync.htm
tech.root: VDS
ms.assetid: 7814b8ef-84b4-453e-b480-c32b67e5af93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsAsync, IVdsAsync interface [VDS], IVdsAsync interface [VDS],described, base.ivdsasync, vds/IVdsAsync, vdshwprv/IVdsAsync
ms.topic: interface
f1_keywords: 
 - "vdshwprv/IVdsAsync"
dev_langs:
 - c++
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAsync interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Manages asynchronous 
   operations. Methods that initiate asynchronous operations return a pointer to an 
   <b>IVdsAsync</b> interface, allowing the caller to optionally 
   cancel, wait for, or query the status of the asynchronous operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsAsync</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels the asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-querystatus">QueryStatus</a>
</td>
<td align="left" width="63%">
Returns when the asynchronous operation is in progress, or has either finished successfully or failed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">Wait</a>
</td>
<td align="left" width="63%">
Returns when the asynchronous operation has either finished successfully or failed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/helper-objects">Helper Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ienumvdsobject-next">IEnumVdsObject::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/managing-asynchronous-operations">Managing Asynchronous Operations</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

