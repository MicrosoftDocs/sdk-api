---
UID: NN:cluadmex.IGetClusterUIInfo
title: IGetClusterUIInfo
author: windows-driver-content
description: Called by a Failover Cluster Administrator extension to retrieve information about Failover Cluster Administrator's user interface.
old-location: mscs\igetclusteruiinfo.htm
old-project: MsCS
ms.assetid: e41afb20-5bb8-475f-a056-53d7be8f4bf0
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IGetClusterUIInfo, IGetClusterUIInfo interface [Failover Cluster], IGetClusterUIInfo interface [Failover Cluster], described, _wolf_igetclusteruiinfo, cluadmex/IGetClusterUIInfo, mscs.igetclusteruiinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IGetClusterUIInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterUIInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Called by a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extension to retrieve 
    information about Failover Cluster Administrator's user interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterUIInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetClusterUIInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetClusterUIInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c892250-80b7-4bf8-9514-64833d0e3450">GetClusterName</a>
</td>
<td align="left" width="63%">
Returns the name of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87dc900d-eee3-4e48-8294-a1d5c3a95179">GetFont</a>
</td>
<td align="left" width="63%">
Returns a handle to the font to be displayed on property and wizard pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4572178-6225-4a22-8b45-7e8abbaa9759">GetIcon</a>
</td>
<td align="left" width="63%">
Returns a handle to the icon to use in the upper-left corner of property and wizard pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ab4e6bb-0aba-4115-b068-171aaf0b7cef">GetLocale</a>
</td>
<td align="left" width="63%">
Returns the locale identifier to be used with property and wizard pages.

</td>
</tr>
</table> 


## -remarks



You can use the <b>IGetClusterUIInfo</b> interface when 
     Failover Cluster Administrator calls your implementations of the following methods:

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
Failover Cluster Administrator passes in an <a href="_com_iunknown">IUnknown</a> 
     interface pointer, <i>piData</i>. Use <i>piData</i> to call 
     <a href="_com_IUnknown_QueryInterface">QueryInterface</a> for one of the 
     <b>IGetClusterUIInfo</b> methods.

Do not obtain other information interfaces, such as 
     <a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterUIInfo</b> interface. While 
     <a href="_com_IUnknown_QueryInterface">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the cluster, and the result is an interface that represents no real 
     cluster object. For an illustration, see 
     <a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cad771e-5640-4024-8552-d83827fb4e8b">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
 

 

