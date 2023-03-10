---
UID: NN:cluadmex.IWEExtendContextMenu
title: IWEExtendContextMenu (cluadmex.h)
description: Implement the IWEExtendContextMenu interface to extend a Failover Cluster Administrator context menu for a cluster object.
helpviewer_keywords: ["IWEExtendContextMenu","IWEExtendContextMenu interface [Failover Cluster]","IWEExtendContextMenu interface [Failover Cluster]","described","_wolf_iweextendcontextmenu","cluadmex/IWEExtendContextMenu","mscs.iweextendcontextmenu"]
old-location: mscs\iweextendcontextmenu.htm
tech.root: MsCS
ms.assetid: a41adde0-fc4f-4997-bb56-5fa43ba62fdb
ms.date: 12/05/2018
ms.keywords: IWEExtendContextMenu, IWEExtendContextMenu interface [Failover Cluster], IWEExtendContextMenu interface [Failover Cluster],described, _wolf_iweextendcontextmenu, cluadmex/IWEExtendContextMenu, mscs.iweextendcontextmenu
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWEExtendContextMenu
 - cluadmex/IWEExtendContextMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IWEExtendContextMenu
---

# IWEExtendContextMenu interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Implement the <b>IWEExtendContextMenu</b> interface to 
    extend a <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> context menu 
    for a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster object</a>.

## -inheritance

The <b>IWEExtendContextMenu</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEExtendContextMenu</b> also has these types of members:

## -remarks

To add code that executes when your context menu items are selected, implement the 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweinvokecommand">IWEInvokeCommand</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweinvokecommand">IWEInvokeCommand</a>
