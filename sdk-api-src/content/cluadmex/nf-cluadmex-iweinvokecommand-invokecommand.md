---
UID: NF:cluadmex.IWEInvokeCommand.InvokeCommand
title: IWEInvokeCommand::InvokeCommand
author: windows-sdk-content
description: Allows you to implement procedures that execute when users select your context menu items.
old-location: mscs\iweinvokecommand_invokecommand.htm
tech.root: mscs
ms.assetid: 1e723535-d786-496f-bc16-5b10a8a22383
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IWEInvokeCommand interface [Failover Cluster],InvokeCommand method, IWEInvokeCommand.InvokeCommand, IWEInvokeCommand::InvokeCommand, InvokeCommand, InvokeCommand method [Failover Cluster], InvokeCommand method [Failover Cluster],IWEInvokeCommand interface, _wolf_iweinvokecommand_invokecommand, cluadmex/IWEInvokeCommand::InvokeCommand, mscs.iweinvokecommand_invokecommand
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
 - IWEInvokeCommand.InvokeCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
       <a href="https://msdn.microsoft.com/en-us/library/Aa370505(v=VS.85).aspx">IWCContextMenuCallback::AddExtensionMenuItem</a> 
       method.


### -param piData [in]


<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface pointer for retrieving information associated with the 
       command identified by <i>nCommandID</i>. By calling the 
       <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method with the <i>piData</i> 
       pointer, the following interfaces are available:

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
Depending on the type of <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster object</a> to 
       which the context menu item applies, a pointer to one of the following interfaces is also available:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370221(v=VS.85).aspx">IGetClusterNodeInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371745(v=VS.85).aspx">node</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>, if the property page 
        relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa369645(v=VS.85).aspx">group</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370219(v=VS.85).aspx">IGetClusterNetworkInfo</a>, if the property 
        page relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371501(v=VS.85).aspx">network</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370217(v=VS.85).aspx">IGetClusterNetInterfaceInfo</a>, if the 
        property page relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa371519(v=VS.85).aspx">network interface</a>.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>, if the property 
        page relates to a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>.</li>
</ul>

## -returns



Returns one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.




## -remarks



To create context menu items and add them to Failover Cluster Administrator, use the 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370713(v=VS.85).aspx">IWEExtendContextMenu::AddContextMenuItems</a> 
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



<a href="https://msdn.microsoft.com/en-us/library/Aa370505(v=VS.85).aspx">IWCContextMenuCallback::AddExtensionMenuItem</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370713(v=VS.85).aspx">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370744(v=VS.85).aspx">IWEInvokeCommand</a>
 

 

