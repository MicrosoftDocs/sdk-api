---
UID: NN:netcon.INetConnection
title: INetConnection
author: windows-sdk-content
description: The INetConnection interface provides methods to manage network connections.
old-location: ics\inetconnection.htm
tech.root: ics
ms.assetid: 7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetConnection, INetConnection interface [ICS/ICF], INetConnection interface [ICS/ICF],described, _ics_inetconnection, ics.inetconnection, netcon/INetConnection
ms.topic: interface
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetConnection interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/en-us/library/Aa366453(v=VS.85).aspx">Windows Firewall API</a>.]

The 
<b>INetConnection</b> interface provides methods to manage network connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff627133-1f48-4a4d-96d5-9a2ef95b6e61">Connect</a>
</td>
<td align="left" width="63%">
Establish the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2179872-da9b-4d89-b6e9-b318d304b15d">Delete</a>
</td>
<td align="left" width="63%">
Delete the network connection from the connections folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa365095(v=VS.85).aspx">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnect the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa365096(v=VS.85).aspx">Duplicate</a>
</td>
<td align="left" width="63%">
Create a duplicate of the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa365097(v=VS.85).aspx">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieve the properties for the network connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33d69dff-8137-4901-9529-31130803b19f">GetUiObjectClassId</a>
</td>
<td align="left" width="63%">
Retrieve the class identifier of the user interface for the connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/741261cd-f86f-4889-aa3a-df3598938883">Rename</a>
</td>
<td align="left" width="63%">
Rename the connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366131(v=VS.85).aspx">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

