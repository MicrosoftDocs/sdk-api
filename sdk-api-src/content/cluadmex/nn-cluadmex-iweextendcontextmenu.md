---
UID: NN:cluadmex.IWEExtendContextMenu
title: IWEExtendContextMenu
author: windows-driver-content
description: Implement the IWEExtendContextMenu interface to extend a Failover Cluster Administrator context menu for a cluster object.
old-location: mscs\iweextendcontextmenu.htm
old-project: MsCS
ms.assetid: a41adde0-fc4f-4997-bb56-5fa43ba62fdb
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWEExtendContextMenu, IWEExtendContextMenu interface [Failover Cluster], IWEExtendContextMenu interface [Failover Cluster],described, _wolf_iweextendcontextmenu, cluadmex/IWEExtendContextMenu, mscs.iweextendcontextmenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 Enterprise, Windows Server 2003 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CluAdmEx.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IWEExtendContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWEExtendContextMenu interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Implement the <b>IWEExtendContextMenu</b> interface to 
    extend a <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> context menu 
    for a <a href="c_gly.htm">cluster object</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWEExtendContextMenu</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWEExtendContextMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWEExtendContextMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">AddContextMenuItems</a>
</td>
<td align="left" width="63%">
Allows you to create context menu items for a cluster object and add them to a Failover Cluster Administrator 
      context menu.

</td>
</tr>
</table> 


## -remarks



To add code that executes when your context menu items are selected, implement the 
     <a href="https://msdn.microsoft.com/53997e65-5011-4c3b-9586-ede9ed693ab5">IWEInvokeCommand</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/a2306e94-47c6-441f-b06d-70e3f633f78e">Failover Cluster Administrator Extension Interfaces</a>



<a href="https://msdn.microsoft.com/53997e65-5011-4c3b-9586-ede9ed693ab5">IWEInvokeCommand</a>
 

 

