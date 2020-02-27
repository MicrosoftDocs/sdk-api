---
UID: NN:cluadmex.IGetClusterNetInterfaceInfo
title: IGetClusterNetInterfaceInfo (cluadmex.h)
description: The IGetClusterNetInterfaceInfo interface is called by a Failover Cluster Administrator extension to retrieve information about a network interface.
old-location: mscs\igetclusternetinterfaceinfo.htm
tech.root: MsCS
ms.assetid: c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79
ms.date: 12/05/2018
ms.keywords: IGetClusterNetInterfaceInfo, IGetClusterNetInterfaceInfo interface [Failover Cluster], IGetClusterNetInterfaceInfo interface [Failover Cluster],described, _wolf_igetclusternetinterfaceinfo, cluadmex/IGetClusterNetInterfaceInfo, mscs.igetclusternetinterfaceinfo
f1_keywords:
- cluadmex/IGetClusterNetInterfaceInfo
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
- IGetClusterNetInterfaceInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGetClusterNetInterfaceInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterNetInterfaceInfo</b> interface 
    is called by a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> 
    extension to retrieve information about a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterNetInterfaceInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetClusterNetInterfaceInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetClusterNetInterfaceInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-igetclusternetinterfaceinfo-getnetinterfacehandle">GetNetInterfaceHandle</a>
</td>
<td align="left" width="63%">
Returns a handle to a network interface.

</td>
</tr>
</table> 


## -remarks



If the object being extended is not a network interface, queries for 
     <b>IGetClusterNetInterfaceInfo</b> methods will 
     fail. Otherwise, you can use the 
     <b>IGetClusterNetInterfaceInfo</b> interface when 
     Failover Cluster Administrator calls your implementations of the following methods.

<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
</li>
</ul>
Failover Cluster Administrator passes in an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for one of the 
     <b>IGetClusterNetInterfaceInfo</b> methods.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator-information-interfaces">Failover Cluster Administrator Information Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
 

 

