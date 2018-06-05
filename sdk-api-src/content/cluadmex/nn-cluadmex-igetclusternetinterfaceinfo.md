---
UID: NN:cluadmex.IGetClusterNetInterfaceInfo
title: IGetClusterNetInterfaceInfo
author: windows-sdk-content
description: The IGetClusterNetInterfaceInfo interface is called by a Failover Cluster Administrator extension to retrieve information about a network interface.
old-location: mscs\igetclusternetinterfaceinfo.htm
old-project: MsCS
ms.assetid: c7a0ee81-e263-4a2d-a0e5-18d3a4ad0d79
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IGetClusterNetInterfaceInfo, IGetClusterNetInterfaceInfo interface [Failover Cluster], IGetClusterNetInterfaceInfo interface [Failover Cluster],described, _wolf_igetclusternetinterfaceinfo, cluadmex/IGetClusterNetInterfaceInfo, mscs.igetclusternetinterfaceinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IGetClusterNetInterfaceInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterNetInterfaceInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterNetInterfaceInfo</b> interface 
    is called by a <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> 
    extension to retrieve information about a 
    <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interface</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterNetInterfaceInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetClusterNetInterfaceInfo</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a11ebbed-72e3-4f57-af8d-8a14c4b0fad2">GetNetInterfaceHandle</a>
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
<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>
</li>
<li>
<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">IWEExtendContextMenu::AddContextMenuItems</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
</li>
</ul>
Failover Cluster Administrator passes in an <a href="_com_iunknown">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="_com_IUnknown_QueryInterface">QueryInterface</a> for one of the 
     <b>IGetClusterNetInterfaceInfo</b> methods.




## -see-also




<a href="https://msdn.microsoft.com/3cad771e-5640-4024-8552-d83827fb4e8b">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
 

 

