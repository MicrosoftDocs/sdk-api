---
UID: NN:wmsdkidl.IWMClientConnections2
title: IWMClientConnections2
author: windows-driver-content
description: The IWMClientConnections2 interface retrieves advanced client information.The writer network sink object exposes this interface.
old-location: wmformat\iwmclientconnections2.htm
old-project: wmformat
ms.assetid: 7148dd13-e5de-4adb-89e7-3f02a463c2d1
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMClientConnections2, IWMClientConnections2 interface [windows Media Format], IWMClientConnections2 interface [windows Media Format], described, IWMClientConnections2Interface, wmformat.iwmclientconnections2, wmsdkidl/IWMClientConnections2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMClientConnections2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMClientConnections2 interface


## -description



The <b>IWMClientConnections2</b> interface retrieves advanced client information.

The writer network sink object exposes this interface. You can retrieve a pointer to this interface by calling the <b>QueryInterface</b> method of any other interface on a writer network sink object.



The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fea7cd85-22ab-4f3b-8a0a-301496f0c788">IWMClientConnections</a>
</td>
<td>IID_IWMClientConnections</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3831b727-7fdc-4d05-a7b3-86ca5b5c3b17">IWMRegisterCallback</a>
</td>
<td>IID_IWMRegisterCallback</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink</a>
</td>
<td>IID_IWMWriterNetworkSink</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table>
 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMClientConnections2</b> interface inherits from <a href="https://msdn.microsoft.com/fea7cd85-22ab-4f3b-8a0a-301496f0c788">IWMClientConnections</a>. <b>IWMClientConnections2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMClientConnections2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39731e6a-cfd7-48c5-9107-bf5373dfeb4a">GetClientInfo</a>
</td>
<td align="left" width="63%">
Retrieves detailed information about a client attached to a writer network sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fea7cd85-22ab-4f3b-8a0a-301496f0c788">IWMClientConnections</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

