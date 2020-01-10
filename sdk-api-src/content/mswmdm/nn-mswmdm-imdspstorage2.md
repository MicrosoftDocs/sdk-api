---
UID: NN:mswmdm.IMDSPStorage2
title: IMDSPStorage2 (mswmdm.h)
description: The IMDSPStorage2 interface extends IMDSPStorage by providing methods for getting and setting extended attributes and making it possible to get a pointer to a storage medium from its name.
old-location: wmdm\imdspstorage2.htm
tech.root: WMDM
ms.assetid: 39afb282-7141-4eb5-93e9-a69bef495d80
ms.date: 12/05/2018
ms.keywords: IMDSPStorage2, IMDSPStorage2 interface [windows Media Device Manager], IMDSPStorage2 interface [windows Media Device Manager],described, IMDSPStorage2Interface, mswmdm/IMDSPStorage2, wmdm.imdspstorage2
f1_keywords:
- mswmdm/IMDSPStorage2
dev_langs:
- c++
req.header: mswmdm.h
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
- mswmdm.h
api_name:
- IMDSPStorage2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPStorage2 interface


## -description



The <b>IMDSPStorage2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a> by providing methods for getting and setting extended attributes and making it possible to get a pointer to a storage medium from its name. This interface also extends the <b>CreateStorage</b> method of the <b>IMDSPStorage</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorage2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage</a>. <b>IMDSPStorage2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorage2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-createstorage2">CreateStorage2</a>
</td>
<td align="left" width="63%">
Creates storage for a file to be copied to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-getattributes2">GetAttributes2</a>
</td>
<td align="left" width="63%">
Gets attributes of files or storages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-getstorage">GetStorage</a>
</td>
<td align="left" width="63%">
Gets a storage pointer and a string containing the name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage2-setattributes2">SetAttributes2</a>
</td>
<td align="left" width="63%">
Sets storage attributes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3">IMDSPStorage3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4">IMDSPStorage4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

