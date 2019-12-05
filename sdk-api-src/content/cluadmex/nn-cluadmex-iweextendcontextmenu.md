---
UID: NN:cluadmex.IWEExtendContextMenu
title: IWEExtendContextMenu (cluadmex.h)
description: Implement the IWEExtendContextMenu interface to extend a Failover Cluster Administrator context menu for a cluster object.
old-location: mscs\iweextendcontextmenu.htm
tech.root: MsCS
ms.assetid: a41adde0-fc4f-4997-bb56-5fa43ba62fdb
ms.date: 12/05/2018
ms.keywords: IWEExtendContextMenu, IWEExtendContextMenu interface [Failover Cluster], IWEExtendContextMenu interface [Failover Cluster],described, _wolf_iweextendcontextmenu, cluadmex/IWEExtendContextMenu, mscs.iweextendcontextmenu
ms.topic: interface
f1_keywords:
- cluadmex/IWEExtendContextMenu
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- cluadmex.h
api_name:
- IWEExtendContextMenu
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWEExtendContextMenu interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Implement the <b>IWEExtendContextMenu</b> interface to 
    extend a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> context menu 
    for a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/c-gly">cluster object</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWEExtendContextMenu</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEExtendContextMenu</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">AddContextMenuItems</a>
</td>
<td align="left" width="63%">
Allows you to create context menu items for a cluster object and add them to a Failover Cluster Administrator 
      context menu.

</td>
</tr>
</table> 


## -remarks



To add code that executes when your context menu items are selected, implement the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweinvokecommand">IWEInvokeCommand</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweinvokecommand">IWEInvokeCommand</a>
 

 

