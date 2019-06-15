---
UID: NN:wtsprotocol.IWRdsWddmIddProps
title: IWRdsWddmIddProps (wtsprotocol.h)
author: windows-sdk-content
description: This interface allows a custom IDD driver to be loaded in a remote session.
old-location: termserv\iwrdswddmiddprops.htm
tech.root: TermServ
ms.assetid: 9473E754-D158-40E7-9E76-D8EA5A4BE86E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsWddmIddProps, IWRdsWddmIddProps interface [Remote Desktop Services], IWRdsWddmIddProps interface [Remote Desktop Services],described, termserv.iwrdswddmiddprops, wtsprotocol/IWRdsWddmIddProps
ms.topic: interface
f1_keywords: ["wtsprotocol/IWRdsWddmIddProps"]
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
ms.custom: 19H1
---

# IWRdsWddmIddProps interface


## -description


This interface allows a custom IDD driver to be loaded in a remote session.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsWddmIddProps</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsWddmIddProps</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Mt832806(v=VS.85).aspx">EnableWddmIdd</a>
</td>
<td align="left" width="63%">
Termsrv uses this method to tell protocol stack  which mode it is 
    operating.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt832807(v=VS.85).aspx">GetHardwareId</a>
</td>
<td align="left" width="63%">
Protocol stack uses this method to return hardware Id of WDDM ID driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt832808(v=VS.85).aspx">OnDriverLoad</a>
</td>
<td align="left" width="63%">
Termsrv uses this method to return a handle of the loaded WDDM ID driver to 
    the protocol stack. From this point the stack owns the handle and needs to call 
    CloseHandle() after communication with the driver is no longer needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt832809(v=VS.85).aspx">OnDriverUnload</a>
</td>
<td align="left" width="63%">
Termsrv uses this method to tell the protocol stack that PnP unloaded the
    WDDM ID driver.

</td>
</tr>
</table> 

