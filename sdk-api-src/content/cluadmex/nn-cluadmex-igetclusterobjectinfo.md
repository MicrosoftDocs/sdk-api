---
UID: NN:cluadmex.IGetClusterObjectInfo
title: IGetClusterObjectInfo (cluadmex.h)
description: Called by a Failover Cluster Administrator extension to retrieve information about a cluster object.
helpviewer_keywords: ["IGetClusterObjectInfo","IGetClusterObjectInfo interface [Failover Cluster]","IGetClusterObjectInfo interface [Failover Cluster]","described","_wolf_igetclusterobjectinfo","cluadmex/IGetClusterObjectInfo","mscs.igetclusterobjectinfo"]
old-location: mscs\igetclusterobjectinfo.htm
tech.root: MsCS
ms.assetid: a88ba05c-b64b-4d6d-b005-f2f867093355
ms.date: 12/05/2018
ms.keywords: IGetClusterObjectInfo, IGetClusterObjectInfo interface [Failover Cluster], IGetClusterObjectInfo interface [Failover Cluster],described, _wolf_igetclusterobjectinfo, cluadmex/IGetClusterObjectInfo, mscs.igetclusterobjectinfo
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
 - IGetClusterObjectInfo
 - cluadmex/IGetClusterObjectInfo
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
 - IGetClusterObjectInfo
---

# IGetClusterObjectInfo interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterObjectInfo</b> interface is 
    called by a <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> 
    extension to retrieve information about a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>.

## -inheritance

The <b>IGetClusterObjectInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetClusterObjectInfo</b> also has these types of members:

## -remarks

You can use the <b>IGetClusterObjectInfo</b> interface 
     when Failover Cluster Administrator calls your implementations of the following methods:

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
     <b>IGetClusterObjectInfo</b> methods.

Do not obtain other information interfaces, such as 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterObjectInfo</b> interface. While 
     <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>, 
     and the result is an interface that represents no real cluster object. For an illustration, see 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-information-interfaces">Failover Cluster Administrator Information Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
