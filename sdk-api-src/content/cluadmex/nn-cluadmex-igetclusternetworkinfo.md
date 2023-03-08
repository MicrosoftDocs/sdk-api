---
UID: NN:cluadmex.IGetClusterNetworkInfo
title: IGetClusterNetworkInfo (cluadmex.h)
description: Called by a Failover Cluster Administrator extension to retrieve information about a network.
helpviewer_keywords: ["IGetClusterNetworkInfo","IGetClusterNetworkInfo interface [Failover Cluster]","IGetClusterNetworkInfo interface [Failover Cluster]","described","_wolf_igetclusternetworkinfo","cluadmex/IGetClusterNetworkInfo","mscs.igetclusternetworkinfo"]
old-location: mscs\igetclusternetworkinfo.htm
tech.root: MsCS
ms.assetid: 7c304d9c-69b6-48fc-bb1b-f49d1ac8ede4
ms.date: 12/05/2018
ms.keywords: IGetClusterNetworkInfo, IGetClusterNetworkInfo interface [Failover Cluster], IGetClusterNetworkInfo interface [Failover Cluster],described, _wolf_igetclusternetworkinfo, cluadmex/IGetClusterNetworkInfo, mscs.igetclusternetworkinfo
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
 - IGetClusterNetworkInfo
 - cluadmex/IGetClusterNetworkInfo
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
 - IGetClusterNetworkInfo
---

# IGetClusterNetworkInfo interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterNetworkInfo</b> interface is 
    called by a <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> 
    extension to retrieve information about a <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.

## -inheritance

The <b>IGetClusterNetworkInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetClusterNetworkInfo</b> also has these types of members:

## -remarks

If the object being extended is not a network, queries for 
     <b>IGetClusterNetworkInfo</b> methods will fail. 
     Otherwise, you can use the 
     <b>IGetClusterNetworkInfo</b> interface when Failover 
     Cluster Administrator calls your implementations of the following methods:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
</li>
</ul>
Failover Cluster Administrator passes in an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for one of the 
     <b>IGetClusterNetworkInfo</b> methods.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-information-interfaces">Failover Cluster Administrator Information Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
