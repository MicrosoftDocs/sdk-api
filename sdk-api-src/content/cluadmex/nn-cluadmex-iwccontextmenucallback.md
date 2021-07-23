---
UID: NN:cluadmex.IWCContextMenuCallback
title: IWCContextMenuCallback (cluadmex.h)
description: The IWCContextMenuCallback interface is called by a Failover Cluster Administrator extension to add items to a Failover Cluster Administrator context menu.
helpviewer_keywords: ["IWCContextMenuCallback","IWCContextMenuCallback interface [Failover Cluster]","IWCContextMenuCallback interface [Failover Cluster]","described","_wolf_iwccontextmenucallback","cluadmex/IWCContextMenuCallback","mscs.iwccontextmenucallback"]
old-location: mscs\iwccontextmenucallback.htm
tech.root: MsCS
ms.assetid: 50dbb062-100a-40af-8e52-7bd4574334f4
ms.date: 12/05/2018
ms.keywords: IWCContextMenuCallback, IWCContextMenuCallback interface [Failover Cluster], IWCContextMenuCallback interface [Failover Cluster],described, _wolf_iwccontextmenucallback, cluadmex/IWCContextMenuCallback, mscs.iwccontextmenucallback
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
 - IWCContextMenuCallback
 - cluadmex/IWCContextMenuCallback
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
 - IWCContextMenuCallback
---

# IWCContextMenuCallback interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IWCContextMenuCallback</b> interface is called by a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extension to add items 
     to a Failover Cluster Administrator context menu.

## -inheritance

The <b>IWCContextMenuCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWCContextMenuCallback</b> also has these types of members:

## -remarks

Use the <i>piCallback</i> pointer that you receive when Failover Cluster Administrator calls 
     your 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a> 
     method to call the <b>IWCContextMenuCallback</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-callback-interfaces">Failover Cluster Administrator Callback Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>
