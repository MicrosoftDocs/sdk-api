---
UID: NN:mswmdm.IMDSPObject2
title: IMDSPObject2 (mswmdm.h)
description: Windows Media Device Manager uses IMDSPObject2 to enable more efficient file reading and writing.Note  Unless the service provider has added the device parameter UseExtendedWmdm with a value of 1, Windows Media Device Manager will not call this interface. See Device Parameters for more information about this. .
old-location: wmdm\imdspobject2.htm
tech.root: WMDM
ms.assetid: f79c07a6-b7e6-4c00-83be-ac2bfc9a751b
ms.date: 12/05/2018
ms.keywords: IMDSPObject2, IMDSPObject2 interface [windows Media Device Manager], IMDSPObject2 interface [windows Media Device Manager],described, IMDSPObject2Interface, mswmdm/IMDSPObject2, wmdm.imdspobject2
f1_keywords:
- mswmdm/IMDSPObject2
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
- IMDSPObject2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPObject2 interface


## -description



Windows Media Device Manager uses <b>IMDSPObject2</b> to enable more efficient file reading and writing.

<div class="alert"><b>Note</b>  Unless the service provider has added the device parameter <b>UseExtendedWmdm</b> with a value of 1, Windows Media Device Manager will not call this interface. See <a href="https://docs.microsoft.com/windows/desktop/WMDM/device-parameters">Device Parameters</a> for more information about this.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPObject2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject</a>. <b>IMDSPObject2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPObject2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel">ReadOnClearChannel</a>
</td>
<td align="left" width="63%">
Reads data from the object at the current position without secure authenticated channel (SAC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel">WriteOnClearChannel</a>
</td>
<td align="left" width="63%">
Writes data to the object at the current position without SAC.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

