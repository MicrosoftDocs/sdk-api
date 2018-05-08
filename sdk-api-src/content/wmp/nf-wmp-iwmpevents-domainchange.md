---
UID: NF:wmp.IWMPEvents.DomainChange
title: IWMPEvents::DomainChange
author: windows-driver-content
description: The DomainChange event occurs when the DVD domain changes.
old-location: wmp\iwmpevents_iwmpevents__domainchange.htm
old-project: WMP
ms.assetid: deb8e05e-a6dc-4971-9c34-9c12f1dedc9e
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: DomainChange, DomainChange method [Windows Media Player], DomainChange method [Windows Media Player],IWMPEvents interface, IWMPEvents interface [Windows Media Player],DomainChange method, IWMPEvents.DomainChange, IWMPEvents::DomainChange, IWMPEventsDomainChange, wmp.iwmpevents_iwmpevents__domainchange, wmp/IWMPEvents::DomainChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPEvents.DomainChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents::DomainChange


## -description



The <b>DomainChange</b> event occurs when the DVD domain changes.




## -parameters




### -param strDomain [in]

Specifies the new domain. It can be one of the following values:

<table>
<tr>
<th>String</th>
<th>Description</th>
</tr>
<tr>
<td>firstPlay</td>
<td>Performing default initialization of a DVD disc.</td>
</tr>
<tr>
<td>videoManagerMenu</td>
<td>Displaying menus for whole disc. Also known as Root Menu or topMenu.</td>
</tr>
<tr>
<td>videoTitleSetMenu</td>
<td>Displaying menus for current title set. Also known as titleMenu</td>
</tr>
<tr>
<td>title</td>
<td>Displaying the current title.</td>
</tr>
<tr>
<td>stop</td>
<td>The DVD Navigator is in the DVD Stop domain.</td>
</tr>
</table>
 


## -returns



This method does not return a value.




## -remarks



<b>Windows Media Player 10 Mobile: </b>This event is not supported.


		Windows XP or later.
		




## -see-also




<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
 

 

