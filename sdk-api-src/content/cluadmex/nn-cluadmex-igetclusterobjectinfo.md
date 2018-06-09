---
UID: NN:cluadmex.IGetClusterObjectInfo
title: IGetClusterObjectInfo
author: windows-sdk-content
description: Called by a Failover Cluster Administrator extension to retrieve information about a cluster object.
old-location: mscs\igetclusterobjectinfo.htm
old-project: MsCS
ms.assetid: a88ba05c-b64b-4d6d-b005-f2f867093355
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IGetClusterObjectInfo, IGetClusterObjectInfo interface [Failover Cluster], IGetClusterObjectInfo interface [Failover Cluster],described, _wolf_igetclusterobjectinfo, cluadmex/IGetClusterObjectInfo, mscs.igetclusterobjectinfo
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
 - IGetClusterObjectInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterObjectInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterObjectInfo</b> interface is 
    called by a <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> 
    extension to retrieve information about a 
    <a href="https://msdn.microsoft.com/609cc002-2db9-4ec6-a802-8f7bdbb11b90">cluster object</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterObjectInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetClusterObjectInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetClusterObjectInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e45f3652-74da-4d93-826d-320ddae10f49">GetObjectName</a>
</td>
<td align="left" width="63%">
Returns the name of a cluster object.</p> (Inherited from <b>IGetClusterObjectInfo</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926847">GetObjectType</a>
</td>
<td align="left" width="63%">
Returns the type of a cluster object.</p> (Inherited from <b>IGetClusterObjectInfo</b>)</td>
</tr>
</table> 


## -remarks



You can use the <b>IGetClusterObjectInfo</b> interface 
     when Failover Cluster Administrator calls your implementations of the following methods:

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
Failover Cluster Administrator passes in an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown.md">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> for one of the 
     <b>IGetClusterObjectInfo</b> methods.

Do not obtain other information interfaces, such as 
     <a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterObjectInfo</b> interface. While 
     <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, 
     and the result is an interface that represents no real cluster object. For an illustration, see 
     <a href="https://msdn.microsoft.com/8a3a9e9d-4666-4d9a-83e3-10d667b42d66">IGetClusterResourceInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cad771e-5640-4024-8552-d83827fb4e8b">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
 

 

