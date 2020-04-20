---
UID: NN:bdaiface.IBDA_NameValueService
title: IBDA_NameValueService (bdaiface.h)
description: Retrieves name/value pairs from a media transform device (MTD) through the device's General Purpose Name Value Service (GPNVS). Name/value pairs are used to get the capabilities of the device.helpviewer_keywords: ["IBDA_NameValueService","IBDA_NameValueService interface [Microsoft TV Technologies]","IBDA_NameValueService interface [Microsoft TV Technologies]","described","bdaiface/IBDA_NameValueService","mstv.ibda_namevalueservice"]
old-location: mstv\ibda_namevalueservice.htm
tech.root: mstv
ms.assetid: 7b6a12d2-24e4-42d8-9138-86c2fe558d86
ms.date: 12/05/2018
ms.keywords: IBDA_NameValueService, IBDA_NameValueService interface [Microsoft TV Technologies], IBDA_NameValueService interface [Microsoft TV Technologies],described, bdaiface/IBDA_NameValueService, mstv.ibda_namevalueservice
f1_keywords:
- bdaiface/IBDA_NameValueService
dev_langs:
- c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
- bdaiface.h
api_name:
- IBDA_NameValueService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_NameValueService interface


## -description


Retrieves name/value pairs from a media transform device (MTD) through the device's General Purpose Name Value Service (GPNVS). Name/value pairs are used to get the capabilities of the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_NameValueService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_NameValueService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_NameValueService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_namevalueservice-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Gets a value by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/dd376218(v=vs.85)">GetValueNameByIndex</a>
</td>
<td align="left" width="63%">
Gets a name, specified by index, from the device's list of name/value pairs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_namevalueservice-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets a name/value pair in device memory.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_NameValueService)</code>.



