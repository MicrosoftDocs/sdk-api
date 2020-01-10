---
UID: NN:vds.IVdsServiceLoader
title: IVdsServiceLoader (vds.h)
description: Instantiates a service loader object.
old-location: base\ivdsserviceloader.htm
tech.root: VDS
ms.assetid: 43533ee7-4e44-48c9-8c9d-0992426d79ba
ms.date: 12/05/2018
ms.keywords: IVdsServiceLoader, IVdsServiceLoader interface [VDS], IVdsServiceLoader interface [VDS],described, base.ivdsserviceloader, vds/IVdsServiceLoader
f1_keywords:
- vds/IVdsServiceLoader
dev_langs:
- c++
req.header: vds.h
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
- IVdsServiceLoader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsServiceLoader interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Instantiates a service loader object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceLoader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsServiceLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsserviceloader-loadservice">LoadService</a>
</td>
<td align="left" width="63%">
Launches VDS on the specified computer and returns a pointer to the service object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

