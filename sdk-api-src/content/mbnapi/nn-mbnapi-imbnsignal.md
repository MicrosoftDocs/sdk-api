---
UID: NN:mbnapi.IMbnSignal
title: IMbnSignal
author: windows-sdk-content
description: Get radio signal quality of a Mobile Broadband connection.
old-location: mbn\imbnsignal.htm
tech.root: mbn
ms.assetid: 2b60d078-ccbd-4cc5-addf-e6e95832b3a1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnSignal, IMbnSignal interface [Microsoft Broadband Networks], IMbnSignal interface [Microsoft Broadband Networks],described, mbn.imbnsignal, mbnapi/IMbnSignal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSignal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnSignal interface


## -description


Get radio signal quality of a Mobile Broadband connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnSignal</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnSignal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnSignal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/028adb54-9c81-4a5b-85f7-5c12ce8d84e4">GetSignalError</a>
</td>
<td align="left" width="63%">
Gets the received signal error rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a580232-4cd2-42f4-a6c7-f777d78241b6">GetSignalStrength</a>
</td>
<td align="left" width="63%">
Gets the signal strength received by the device.

</td>
</tr>
</table> 


## -remarks



The calling application can acquire this interface by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>




