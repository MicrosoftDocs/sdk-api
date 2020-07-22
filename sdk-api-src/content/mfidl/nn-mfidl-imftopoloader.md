---
UID: NN:mfidl.IMFTopoLoader
title: IMFTopoLoader (mfidl.h)
description: Converts a partial topology into a full topology.
helpviewer_keywords: ["5ebf117c-e60a-40f2-a24b-c4f9dbdae942","IMFTopoLoader","IMFTopoLoader interface [Media Foundation]","IMFTopoLoader interface [Media Foundation]","described","mf.imftopoloader","mfidl/IMFTopoLoader"]
old-location: mf\imftopoloader.htm
tech.root: mf
ms.assetid: 5ebf117c-e60a-40f2-a24b-c4f9dbdae942
ms.date: 12/05/2018
ms.keywords: 5ebf117c-e60a-40f2-a24b-c4f9dbdae942, IMFTopoLoader, IMFTopoLoader interface [Media Foundation], IMFTopoLoader interface [Media Foundation],described, mf.imftopoloader, mfidl/IMFTopoLoader
f1_keywords:
- mfidl/IMFTopoLoader
dev_langs:
- c++
req.header: mfidl.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFTopoLoader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTopoLoader interface


## -description


Converts a partial topology into a full topology. The topology loader exposes this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopoLoader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopoLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopoLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load">Load</a>
</td>
<td align="left" width="63%">
Creates a fully loaded topology from the input partial topology.

</td>
</tr>
</table> 


## -remarks



To create the topology loader, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader">MFCreateTopoLoader</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/advanced-topology-building">Advanced Topology Building</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/topologies">Topologies</a>
 

 

