---
UID: NF:cluadmex.IWEExtendContextMenu.AddContextMenuItems
title: IWEExtendContextMenu::AddContextMenuItems (cluadmex.h)
description: Allows you to create context menu items for a cluster object and add the items to a Failover Cluster Administrator context menu.
helpviewer_keywords: ["AddContextMenuItems","AddContextMenuItems method [Failover Cluster]","AddContextMenuItems method [Failover Cluster]","IWEExtendContextMenu interface","IWEExtendContextMenu interface [Failover Cluster]","AddContextMenuItems method","IWEExtendContextMenu.AddContextMenuItems","IWEExtendContextMenu::AddContextMenuItems","_wolf_iweextendcontextmenu_addcontextmenuitems","cluadmex/IWEExtendContextMenu::AddContextMenuItems","mscs.iweextendcontextmenu_addcontextmenuitems"]
old-location: mscs\iweextendcontextmenu_addcontextmenuitems.htm
tech.root: MsCS
ms.assetid: 48de3627-a919-437b-b19b-374327234df9
ms.date: 12/05/2018
ms.keywords: AddContextMenuItems, AddContextMenuItems method [Failover Cluster], AddContextMenuItems method [Failover Cluster],IWEExtendContextMenu interface, IWEExtendContextMenu interface [Failover Cluster],AddContextMenuItems method, IWEExtendContextMenu.AddContextMenuItems, IWEExtendContextMenu::AddContextMenuItems, _wolf_iweextendcontextmenu_addcontextmenuitems, cluadmex/IWEExtendContextMenu::AddContextMenuItems, mscs.iweextendcontextmenu_addcontextmenuitems
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
 - IWEExtendContextMenu::AddContextMenuItems
 - cluadmex/IWEExtendContextMenu::AddContextMenuItems
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
 - IWEExtendContextMenu.AddContextMenuItems
---

# IWEExtendContextMenu::AddContextMenuItems


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create context menu items for a cluster object and add the items to a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> context menu.

## -parameters

### -param piData [in]

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer for retrieving information relating to the new menu 
       item. By calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method with the 
       <i>piData</i> pointer, the following interfaces are available:

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
Depending on the type of <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster object</a> for 
       which the context menu is being created, one of the following interfaces may also be available:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternodeinfo">IGetClusterNodeInfo</a>, if the menu item 
        relates to a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>, if the menu item 
        relates to a <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetworkinfo">IGetClusterNetworkInfo</a>, if the menu item 
        relates to a <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetinterfaceinfo">IGetClusterNetInterfaceInfo</a>, if the 
        menu item relates to a <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>, if the menu 
        item relates to a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>.</li>
</ul>

### -param piCallback [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwccontextmenucallback">IWCContextMenuCallback</a> 
       interface implementation for adding new items to the Cluster Administrator context menu.

## -returns

Return one of the following values or any <b>HRESULT</b> that describes the results of 
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
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
At least one of the parameters is invalid.

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
The extension does not support adding context menu items.

</td>
</tr>
</table>

## -remarks

<p class="proch"><b>To implement AddContextMenuItems</b>

<ol>
<li>Call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method pointed to by 
      <i>piData</i> to retrieve a pointer to an interface that can provide information about the 
      object associated with the menu item.</li>
<li>Call the 
      <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwccontextmenucallback-addextensionmenuitem">IWCContextMenuCallback::AddExtensionMenuItem</a> 
      method using the <i>piCallback</i> pointer to add the item to the menu.</li>
</ol>
To add context menu items and to implement code that executes when your context menu items are selected, 
     implement the 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a> 
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



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwccontextmenucallback">IWCContextMenuCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwccontextmenucallback-addextensionmenuitem">IWCContextMenuCallback::AddExtensionMenuItem</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendcontextmenu">IWEExtendContextMenu</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>