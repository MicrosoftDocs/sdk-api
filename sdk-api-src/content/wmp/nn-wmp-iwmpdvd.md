---
UID: NN:wmp.IWMPDVD
title: IWMPDVD
author: windows-sdk-content
description: The IWMPDVD interface provides methods for working with DVDs.
old-location: wmp\iwmpdvd.htm
tech.root: WMP
ms.assetid: d133f1e1-cbeb-403d-b247-9f495cb6f0f7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPDVD, IWMPDVD interface [Windows Media Player], IWMPDVD interface [Windows Media Player],described, IWMPDVDInterface, wmp.iwmpdvd, wmp/IWMPDVD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmp.h
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
 - wmp.h
api_name:
 - IWMPDVD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPDVD interface


## -description



The <b>IWMPDVD</b> interface provides methods for working with DVDs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPDVD</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPDVD</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPDVD</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89d3c8e2-4517-45db-a20c-961089ee8845">back</a>
</td>
<td align="left" width="63%">
Changes the display from a submenu to its parent menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a8d5ea6-ed70-4952-810c-215acd1ae560">get_domain</a>
</td>
<td align="left" width="63%">
Retrieves the current domain of the DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc8ce504-c387-4e3b-a227-926ae26ea78b">get_isAvailable</a>
</td>
<td align="left" width="63%">
Determines whether a specified type of information is available or a given action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0817edb-49af-48b8-82d0-a8c0a827f290">resume</a>
</td>
<td align="left" width="63%">
Changes to playback mode from menu mode, resuming at the same position as when the menu was invoked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93a06367-5b0b-421d-abef-f6cd23e5b0d5">titleMenu</a>
</td>
<td align="left" width="63%">
Stops playback and displays the title menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b96763f-a174-45df-b988-955f9619a4c1">topMenu</a>
</td>
<td align="left" width="63%">
Stops playback and displays the root menu.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPDVD</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/5f839bfe-bf67-49eb-8743-57713e1be7c5">IWMPCore2</a>
</td>
<td>
<a href="https://msdn.microsoft.com/b20a0661-b54b-4953-81df-499c19611a15">get_dvd</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

