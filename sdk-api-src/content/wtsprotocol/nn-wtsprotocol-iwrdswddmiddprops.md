---
UID: NN:wtsprotocol.IWRdsWddmIddProps
title: IWRdsWddmIddProps
author: windows-sdk-content
description: This interface allows a custom IDD driver to be loaded in a remote session.
old-location: termserv\iwrdswddmiddprops.htm
tech.root: termserv
ms.assetid: 9473E754-D158-40E7-9E76-D8EA5A4BE86E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsWddmIddProps, IWRdsWddmIddProps interface [Remote Desktop Services], IWRdsWddmIddProps interface [Remote Desktop Services],described, termserv.iwrdswddmiddprops, wtsprotocol/IWRdsWddmIddProps
ms.topic: interface
req.header: wtsprotocol.h
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
 - Wtsprotocol.h
api_name:
 - IWRdsWddmIddProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsWddmIddProps interface


## -description


This interface allows a custom IDD driver to be loaded in a remote session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsWddmIddProps</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsWddmIddProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsWddmIddProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19F07236-6F9C-49F0-B100-E02F9DBF54F7">EnableWddmIdd</a>
</td>
<td align="left" width="63%">
Termsrv uses this method to tell protocol stack  which mode it is 
    operating.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4F9D2C6D-6555-4ABE-B856-6DD59B139978">GetHardwareId</a>
</td>
<td align="left" width="63%">
Protocol stack uses this method to return hardware Id of WDDM ID driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8070441A-60E1-4752-A987-A5BD322AA55A">OnDriverLoad</a>
</td>
<td align="left" width="63%">
Termsrv uses this method to return a handle of the loaded WDDM ID driver to 
    the protocol stack. From this point the stack owns the handle and needs to call 
    CloseHandle() after communication with the driver is no longer needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D61C38FD-0298-4363-8A09-D0C2844C23CA">OnDriverUnload</a>
</td>
<td align="left" width="63%">
Termsrv uses this method to tell the protocol stack that PnP unloaded the
    WDDM ID driver.

</td>
</tr>
</table> 

