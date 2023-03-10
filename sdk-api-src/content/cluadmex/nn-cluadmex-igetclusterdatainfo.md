---
UID: NN:cluadmex.IGetClusterDataInfo
title: IGetClusterDataInfo (cluadmex.h)
description: The IGetClusterDataInfo interface is called by a Failover Cluster Administrator extension to retrieve information about a cluster.
helpviewer_keywords: ["IGetClusterDataInfo","IGetClusterDataInfo interface [Failover Cluster]","IGetClusterDataInfo interface [Failover Cluster]","described","_wolf_igetclusterdatainfo","cluadmex/IGetClusterDataInfo","mscs.igetclusterdatainfo"]
old-location: mscs\igetclusterdatainfo.htm
tech.root: MsCS
ms.assetid: a2800ac8-a865-4e66-8147-90e95b54cb0c
ms.date: 12/05/2018
ms.keywords: IGetClusterDataInfo, IGetClusterDataInfo interface [Failover Cluster], IGetClusterDataInfo interface [Failover Cluster],described, _wolf_igetclusterdatainfo, cluadmex/IGetClusterDataInfo, mscs.igetclusterdatainfo
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
 - IGetClusterDataInfo
 - cluadmex/IGetClusterDataInfo
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
 - IGetClusterDataInfo
---

# IGetClusterDataInfo interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterDataInfo</b> interface is called by a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extension to retrieve 
    information about a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>.

## -inheritance

The <b>IGetClusterDataInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetClusterDataInfo</b> also has these types of members:

## -remarks

You can use the <b>IGetClusterDataInfo</b> interface when 
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
Failover Cluster Administrator passes in an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer as the 
     <i>piData</i> parameter for these methods. Use <i>piData</i> to call the 
     <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method for one of the 
     <b>IGetClusterDataInfo</b> methods.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-information-interfaces">Failover Cluster Administrator Information Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
