---
UID: NF:cluadmex.IWEInvokeCommand.InvokeCommand
title: IWEInvokeCommand::InvokeCommand (cluadmex.h)
description: Allows you to implement procedures that execute when users select your context menu items.
helpviewer_keywords: ["IWEInvokeCommand interface [Failover Cluster]","InvokeCommand method","IWEInvokeCommand.InvokeCommand","IWEInvokeCommand::InvokeCommand","InvokeCommand","InvokeCommand method [Failover Cluster]","InvokeCommand method [Failover Cluster]","IWEInvokeCommand interface","_wolf_iweinvokecommand_invokecommand","cluadmex/IWEInvokeCommand::InvokeCommand","mscs.iweinvokecommand_invokecommand"]
old-location: mscs\iweinvokecommand_invokecommand.htm
tech.root: MsCS
ms.assetid: 1e723535-d786-496f-bc16-5b10a8a22383
ms.date: 12/05/2018
ms.keywords: IWEInvokeCommand interface [Failover Cluster],InvokeCommand method, IWEInvokeCommand.InvokeCommand, IWEInvokeCommand::InvokeCommand, InvokeCommand, InvokeCommand method [Failover Cluster], InvokeCommand method [Failover Cluster],IWEInvokeCommand interface, _wolf_iweinvokecommand_invokecommand, cluadmex/IWEInvokeCommand::InvokeCommand, mscs.iweinvokecommand_invokecommand
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
 - IWEInvokeCommand::InvokeCommand
 - cluadmex/IWEInvokeCommand::InvokeCommand
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
 - IWEInvokeCommand.InvokeCommand
---

# IWEInvokeCommand::InvokeCommand


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to implement procedures that execute when users select your context menu items.

## -parameters

### -param nCommandID [in]

Identifier of the menu item containing the command to perform. The identifier represented by 
       <i>nCommandID</i> is the identifier passed to the 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwccontextmenucallback-addextensionmenuitem">IWCContextMenuCallback::AddExtensionMenuItem</a> 
       method.

### -param piData [in]

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer for retrieving information associated with the 
       command identified by <i>nCommandID</i>. By calling the 
       <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method with the <i>piData</i> 
       pointer, the following interfaces are available:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterdatainfo">IGetClusterDataInfo</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterobjectinfo">IGetClusterObjectInfo</a>
</li>
</ul>
Depending on the type of <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster object</a> to 
       which the context menu item applies, a pointer to one of the following interfaces is also available:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternodeinfo">IGetClusterNodeInfo</a>, if the property page 
        relates to a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>, if the property page 
        relates to a <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetworkinfo">IGetClusterNetworkInfo</a>, if the property 
        page relates to a <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetinterfaceinfo">IGetClusterNetInterfaceInfo</a>, if the 
        property page relates to a <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>, if the property 
        page relates to a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>.</li>
</ul>

## -returns

Returns one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
<dt>0x80004001</dt>
</dl>
</td>
<td width="60%">
The operation is not implemented by this method.

</td>
</tr>
</table>

## -remarks

To create context menu items and add them to Failover Cluster Administrator, use the 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a> 
     method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterdatainfo">IGetClusterDataInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetinterfaceinfo">IGetClusterNetInterfaceInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetworkinfo">IGetClusterNetworkInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternodeinfo">IGetClusterNodeInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterobjectinfo">IGetClusterObjectInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwccontextmenucallback-addextensionmenuitem">IWCContextMenuCallback::AddExtensionMenuItem</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweinvokecommand">IWEInvokeCommand</a>