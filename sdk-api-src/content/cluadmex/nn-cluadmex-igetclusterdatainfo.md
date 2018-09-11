---
UID: NN:cluadmex.IGetClusterDataInfo
title: IGetClusterDataInfo
author: windows-sdk-content
description: The IGetClusterDataInfo interface is called by a Failover Cluster Administrator extension to retrieve information about a cluster.
old-location: mscs\igetclusterdatainfo.htm
tech.root: mscs
ms.assetid: a2800ac8-a865-4e66-8147-90e95b54cb0c
ms.author: windowssdkdev
ms.date: 08/29/2018
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
 - IGetClusterDataInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterDataInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterDataInfo</b> interface is called by a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> extension to retrieve 
    information about a <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterDataInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IGetClusterDataInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa370212(v=VS.85).aspx">GetClusterHandle</a>
</td>
<td align="left" width="63%">
Returns a handle to the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370213(v=VS.85).aspx">GetClusterName</a>
</td>
<td align="left" width="63%">
Returns the name of the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370214(v=VS.85).aspx">GetObjectCount</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa370720(v=VS.85).aspx">IWEExtendPropertySheet::CreatePropertySheetPages</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370713(v=VS.85).aspx">IWEExtendContextMenu::AddContextMenuItems</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370738(v=VS.85).aspx">IWEExtendWizard::CreateWizardPages</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa370746(v=VS.85).aspx">IWEInvokeCommand::InvokeCommand</a>
</li>
</ul>
Failover Cluster Administrator passes in an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer as the 
     <i>piData</i> parameter for these methods. Use <i>piData</i> to call the 
     <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method for one of the 
     <b>IGetClusterDataInfo</b> methods.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369074(v=VS.85).aspx">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370713(v=VS.85).aspx">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370720(v=VS.85).aspx">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370738(v=VS.85).aspx">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370746(v=VS.85).aspx">IWEInvokeCommand::InvokeCommand</a>
 

 

