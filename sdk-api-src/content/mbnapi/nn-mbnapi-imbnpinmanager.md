---
UID: NN:mbnapi.IMbnPinManager
title: IMbnPinManager
author: windows-sdk-content
description: Provides important details about the device PIN.
old-location: mbn\imbnpinmanager.htm
old-project: mbn
ms.assetid: b5cfabc7-81f8-4ea0-b6f4-5de011320f0b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMbnPinManager, IMbnPinManager interface [Microsoft Broadband Networks], IMbnPinManager interface [Microsoft Broadband Networks],described, mbn.imbnpinmanager, mbnapi/IMbnPinManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnPinManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnPinManager interface


## -description


Provides important details about the device PIN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPinManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnPinManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnPinManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21752fb9-db6b-4fd1-9c6f-a756408bda53">GetPin</a>
</td>
<td align="left" width="63%">
Gets the device PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/732906dd-7d1e-49a1-a3cc-60075eed9c7c">GetPinList</a>
</td>
<td align="left" width="63%">
Gets a list of different PIN types supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34378403-cf58-4ada-9eb6-f5dad5f69bc9">GetPinState</a>
</td>
<td align="left" width="63%">
Gets the current PIN state of the device.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.



