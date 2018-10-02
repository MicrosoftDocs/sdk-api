---
UID: NF:cluadmex.IWEExtendContextMenu.AddContextMenuItems
title: IWEExtendContextMenu::AddContextMenuItems
author: windows-sdk-content
description: Allows you to create context menu items for a cluster object and add the items to a Failover Cluster Administrator context menu.
old-location: mscs\iweextendcontextmenu_addcontextmenuitems.htm
tech.root: MsCS
ms.assetid: 48de3627-a919-437b-b19b-374327234df9
ms.author: windowssdkdev
ms.date: 09/26/2018
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
    <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> context menu.


## -parameters




### -param piData [in]


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer for retrieving information relating to the new menu 
       item. By calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method with the 
       <i>piData</i> pointer, the following interfaces are available:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370234(v=VS.85).aspx">IGetClusterUIInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370211(v=VS.85).aspx">IGetClusterDataInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>
</li>
</ul>
Depending on the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> for 
       which the context menu is being created, one of the following interfaces may also be available:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370221(v=VS.85).aspx">IGetClusterNodeInfo</a>, if the menu item 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>, if the menu item 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>, if the menu item 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370217(v=VS.85).aspx">IGetClusterNetInterfaceInfo</a>, if the 
        menu item relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>, if the menu 
        item relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>.</li>
</ul>

### -param piCallback [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa370501(v=VS.85).aspx">IWCContextMenuCallback</a> 
       interface implementation for adding new items to the Cluster Administrator context menu.


## -returns



Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To implement AddContextMenuItems</b>

<ol>
<li>Call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method pointed to by 
      <i>piData</i> to retrieve a pointer to an interface that can provide information about the 
      object associated with the menu item.</li>
<li>Call the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa370505(v=VS.85).aspx">IWCContextMenuCallback::AddExtensionMenuItem</a> 
      method using the <i>piCallback</i> pointer to add the item to the menu.</li>
</ol>
To add context menu items and to implement code that executes when your context menu items are selected, 
     implement the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370746(v=VS.85).aspx">IWEInvokeCommand::InvokeCommand</a> 
     method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370211(v=VS.85).aspx">IGetClusterDataInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370217(v=VS.85).aspx">IGetClusterNetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370221(v=VS.85).aspx">IGetClusterNodeInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370224(v=VS.85).aspx">IGetClusterObjectInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370234(v=VS.85).aspx">IGetClusterUIInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370501(v=VS.85).aspx">IWCContextMenuCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370505(v=VS.85).aspx">IWCContextMenuCallback::AddExtensionMenuItem</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370711(v=VS.85).aspx">IWEExtendContextMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370746(v=VS.85).aspx">IWEInvokeCommand::InvokeCommand</a>
 

 

