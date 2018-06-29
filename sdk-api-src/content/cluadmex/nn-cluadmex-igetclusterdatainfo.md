---
UID: NN:cluadmex.IGetClusterDataInfo
title: IGetClusterDataInfo
author: windows-sdk-content
description: The IGetClusterDataInfo interface is called by a Failover Cluster Administrator extension to retrieve information about a cluster.
old-location: mscs\igetclusterdatainfo.htm
old-project: MsCS
ms.assetid: a2800ac8-a865-4e66-8147-90e95b54cb0c
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IGetClusterDataInfo, IGetClusterDataInfo interface [Failover Cluster], IGetClusterDataInfo interface [Failover Cluster],described, _wolf_igetclusterdatainfo, cluadmex/IGetClusterDataInfo, mscs.igetclusterdatainfo
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterDataInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterDataInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterDataInfo</b> interface is called by a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extension to retrieve 
    information about a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterDataInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetClusterDataInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetClusterDataInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5623552e-ab06-4e18-88dc-e297c6af8a63">GetClusterHandle</a>
</td>
<td align="left" width="63%">
Returns a handle to the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/711a193f-de29-4e90-adf1-6dc6e95c0c61">GetClusterName</a>
</td>
<td align="left" width="63%">
Returns the name of the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20ef63e2-bcec-48bc-86e8-ab746fb72cc5">GetObjectCount</a>
</td>
<td align="left" width="63%">
Returns a count of the number of selected objects.

</td>
</tr>
</table> 


## -remarks



You can use the <b>IGetClusterDataInfo</b> interface when 
     Cluster Administrator calls your implementations of the following methods:

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
Failover Cluster Administrator passes in an <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer as the 
     <i>piData</i> parameter for these methods. Use <i>piData</i> to call the 
     <a href="https://msdn.microsoft.com/library/Dd757101(v=VS.85).aspx">QueryInterface</a> method for one of the 
     <b>IGetClusterDataInfo</b> methods.




## -see-also




<a href="https://msdn.microsoft.com/3cad771e-5640-4024-8552-d83827fb4e8b">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
 

 

