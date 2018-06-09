---
UID: NN:bdaiface.IBDA_NameValueService
title: IBDA_NameValueService
author: windows-sdk-content
description: Retrieves name/value pairs from a media transform device (MTD) through the device's General Purpose Name Value Service (GPNVS). Name/value pairs are used to get the capabilities of the device.
old-location: mstv\ibda_namevalueservice.htm
old-project: mstv
ms.assetid: 7b6a12d2-24e4-42d8-9138-86c2fe558d86
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IBDA_NameValueService, IBDA_NameValueService interface [Microsoft TV Technologies], IBDA_NameValueService interface [Microsoft TV Technologies],described, bdaiface/IBDA_NameValueService, mstv.ibda_namevalueservice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_NameValueService
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_NameValueService interface


## -description


Retrieves name/value pairs from a media transform device (MTD) through the device's General Purpose Name Value Service (GPNVS). Name/value pairs are used to get the capabilities of the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_NameValueService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_NameValueService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Gets a value by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a860535-db03-4db7-912c-16b7e920151a">GetValueNameByIndex</a>
</td>
<td align="left" width="63%">
Gets a name, specified by index, from the device's list of name/value pairs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets a name/value pair in device memory.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_NameValueService)</code>.



