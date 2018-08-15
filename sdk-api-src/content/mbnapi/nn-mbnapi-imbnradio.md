---
UID: NN:mbnapi.IMbnRadio
title: IMbnRadio
author: windows-sdk-content
description: The IMbnRadio interface is used to query and update the radio state of Mobile Broadband devices.
old-location: mbn\imbnradio.htm
old-project: mbn
ms.assetid: b4b5ccfc-6cbf-4090-aee1-ee97092147f7
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnRadio, IMbnRadio interface [Microsoft Broadband Networks], IMbnRadio interface [Microsoft Broadband Networks],described, mbn.imbnradio, mbnapi/IMbnRadio
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRadio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnRadio interface


## -description


The <b>IMbnRadio</b> interface is used to query and update the radio state of Mobile Broadband devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRadio</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnRadio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnRadio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d140109d-5659-42aa-b645-996dfc5a9d4e">SetSoftwareRadioState</a>
</td>
<td align="left" width="63%">
Sets the software radio state.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRadio</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2958a443-b4c2-43f3-b0b3-956c6b2dca2d">HardwareRadioState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The hardware radio state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8e8cd410-0c8b-4e62-ab8e-65e67f7a81a5">SoftwareRadioState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The software radio state.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.



