---
UID: NF:cluadmex.IWEExtendContextMenu.AddContextMenuItems
title: IWEExtendContextMenu::AddContextMenuItems
author: windows-sdk-content
description: Allows you to create context menu items for a cluster object and add the items to a Failover Cluster Administrator context menu.
old-location: mscs\iweextendcontextmenu_addcontextmenuitems.htm
tech.root: mscs
ms.assetid: 48de3627-a919-437b-b19b-374327234df9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddContextMenuItems, AddContextMenuItems method [Failover Cluster], AddContextMenuItems method [Failover Cluster],IWEExtendContextMenu interface, IWEExtendContextMenu interface [Failover Cluster],AddContextMenuItems method, IWEExtendContextMenu.AddContextMenuItems, IWEExtendContextMenu::AddContextMenuItems, _wolf_iweextendcontextmenu_addcontextmenuitems, cluadmex/IWEExtendContextMenu::AddContextMenuItems, mscs.iweextendcontextmenu_addcontextmenuitems
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWEExtendContextMenu.AddContextMenuItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWEExtendContextMenu::AddContextMenuItems


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create context menu items for a cluster object and add the items to a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> context menu.


## -parameters




### -param piData [in]


<a href="_com_iunknown">IUnknown</a> interface pointer for retrieving information relating to the new menu 
       item. By calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method with the 
       <i>piData</i> pointer, the following interfaces are available:

<ul>
<li>
<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a88ba05c-b64b-4d6d-b005-f2f867093355">IGetClusterObjectInfo</a>
</li>
</ul>
Depending on the type of <a href="c_gly.htm">cluster object</a> for 
       which the context menu is being created, one of the following interfaces may also be available:

<ul>
<li>
<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>, if the menu item 
        relates to a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.</li>
<li>
<a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>, if the menu item 
        relates to a <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a>.</li>
<li>
<a href="https://msdn.microsoft.com/7c304d9c-69b6-48fc-bb1b-f49d1ac8ede4">IGetClusterNetworkInfo</a>, if the menu item 
        relates to a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>.</li>
<li>
<a href="https://msdn.microsoft.com/c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79">IGetClusterNetInterfaceInfo</a>, if the 
        menu item relates to a <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.</li>
<li>
<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>, if the menu 
        item relates to a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.</li>
</ul>

### -param piCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/50dbb062-100a-40af-8e52-7bd4574334f4">IWCContextMenuCallback</a> 
       interface implementation for adding new items to the Cluster Administrator context menu.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To implement AddContextMenuItems</b>

<ol>
<li>Call the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method pointed to by 
      <i>piData</i> to retrieve a pointer to an interface that can provide information about the 
      object associated with the menu item.</li>
<li>Call the 
      <a href="https://msdn.microsoft.com/0eedc564-c82d-4309-b11c-c87d2e73c2c9">IWCContextMenuCallback::AddExtensionMenuItem</a> 
      method using the <i>piCallback</i> pointer to add the item to the menu.</li>
</ol>
To add context menu items and to implement code that executes when your context menu items are selected, 
     implement the 
     <a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a> 
     method.




## -see-also




<a href="https://msdn.microsoft.com/a2800ac8-a865-4e66-8147-90e95b54cb0c">IGetClusterDataInfo</a>



<a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>



<a href="https://msdn.microsoft.com/c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79">IGetClusterNetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/7c304d9c-69b6-48fc-bb1b-f49d1ac8ede4">IGetClusterNetworkInfo</a>



<a href="https://msdn.microsoft.com/97c90830-1f6d-4f8f-ba0a-fee39aef5c1d">IGetClusterNodeInfo</a>



<a href="https://msdn.microsoft.com/a88ba05c-b64b-4d6d-b005-f2f867093355">IGetClusterObjectInfo</a>



<a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>



<a href="https://msdn.microsoft.com/e41afb20-5bb8-475f-a056-53d7be8f4bf0">IGetClusterUIInfo</a>



<a href="https://msdn.microsoft.com/50dbb062-100a-40af-8e52-7bd4574334f4">IWCContextMenuCallback</a>



<a href="https://msdn.microsoft.com/0eedc564-c82d-4309-b11c-c87d2e73c2c9">IWCContextMenuCallback::AddExtensionMenuItem</a>



<a href="https://msdn.microsoft.com/a41adde0-fc4f-4997-bb56-5fa43ba62fdb">IWEExtendContextMenu</a>



<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
 

 

