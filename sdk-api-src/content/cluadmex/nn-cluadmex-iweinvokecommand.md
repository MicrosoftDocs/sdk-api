---
UID: NN:cluadmex.IWEInvokeCommand
title: IWEInvokeCommand (cluadmex.h)
description: Failover Cluster Administrator calls your implementation of the IWEInvokeCommand interface when users select context menu items that you created with the IWEExtendContextMenu interface.
old-location: mscs\iweinvokecommand.htm
tech.root: MsCS
ms.assetid: 53997e65-5011-4c3b-9586-ede9ed693ab5
ms.date: 12/05/2018
ms.keywords: IWEInvokeCommand, IWEInvokeCommand interface [Failover Cluster], IWEInvokeCommand interface [Failover Cluster],described, _wolf_iweinvokecommand, cluadmex/IWEInvokeCommand, mscs.iweinvokecommand
f1_keywords:
- cluadmex/IWEInvokeCommand
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
- IWEInvokeCommand
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWEInvokeCommand interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Failover Cluster Administrator calls your implementation of the 
    <b>IWEInvokeCommand</b> interface when users select context 
    menu items that you created with the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendcontextmenu">IWEExtendContextMenu</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWEInvokeCommand</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEInvokeCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWEInvokeCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">InvokeCommand</a>
</td>
<td align="left" width="63%">
Allows you to implement procedures that execute when users select your context menu items.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendcontextmenu">IWEExtendContextMenu</a>
 

 

