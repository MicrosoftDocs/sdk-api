---
UID: NN:vidcap.IKsNodeControl
title: IKsNodeControl
author: windows-sdk-content
description: The IKsNodeControl interface must be implemented by USB Video Class (UVC) extension units.
old-location: dshow\iksnodecontrol.htm
tech.root: DirectShow
ms.assetid: c38ce847-726a-4c1a-9276-810385af6c9f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IKsNodeControl, IKsNodeControl interface [DirectShow], IKsNodeControl interface [DirectShow],described, IKsNodeControlInterface, dshow.iksnodecontrol, vidcap/IKsNodeControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Vidcap.h
api_name:
 - IKsNodeControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsNodeControl interface


## -description



The <code>IKsNodeControl</code> interface must be implemented by USB Video Class (UVC) extension units. A UVC extension unit is a COM object that provides extended functionality to a USB video device, beyond the functionality provided by the UVC class driver.

The <code>IKsNodeControl</code> interface is used by the KsProxy filter to communicate with the extension unit. Applications do not use this interface. For more information, see the topic "USB Video Class Extension Units" in the Windows DDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IKsNodeControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IKsNodeControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IKsNodeControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/145967fc-3124-4e3b-b1ce-a381ea97cb89">put_KsControl</a>
</td>
<td align="left" width="63%">
Provides an instance of the <b>IKsControl</b> interface to the extension unit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f18085c-5a5c-4bc3-84e2-50fbf2319072">put_NodeId</a>
</td>
<td align="left" width="63%">
Sets the node identifier for the extension unit.

</td>
</tr>
</table> 

