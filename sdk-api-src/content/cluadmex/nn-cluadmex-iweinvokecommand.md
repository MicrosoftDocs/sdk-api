---
UID: NN:cluadmex.IWEInvokeCommand
title: IWEInvokeCommand (cluadmex.h)
description: Failover Cluster Administrator calls your implementation of the IWEInvokeCommand interface when users select context menu items that you created with the IWEExtendContextMenu interface.
helpviewer_keywords: ["IWEInvokeCommand","IWEInvokeCommand interface [Failover Cluster]","IWEInvokeCommand interface [Failover Cluster]","described","_wolf_iweinvokecommand","cluadmex/IWEInvokeCommand","mscs.iweinvokecommand"]
old-location: mscs\iweinvokecommand.htm
tech.root: MsCS
ms.assetid: 53997e65-5011-4c3b-9586-ede9ed693ab5
ms.date: 12/05/2018
ms.keywords: IWEInvokeCommand, IWEInvokeCommand interface [Failover Cluster], IWEInvokeCommand interface [Failover Cluster],described, _wolf_iweinvokecommand, cluadmex/IWEInvokeCommand, mscs.iweinvokecommand
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
 - IWEInvokeCommand
 - cluadmex/IWEInvokeCommand
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
 - IWEInvokeCommand
---

# IWEInvokeCommand interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Failover Cluster Administrator calls your implementation of the 
    <b>IWEInvokeCommand</b> interface when users select context 
    menu items that you created with the 
    <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendcontextmenu">IWEExtendContextMenu</a> interface.

## -inheritance

The <b>IWEInvokeCommand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEInvokeCommand</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendcontextmenu">IWEExtendContextMenu</a>
