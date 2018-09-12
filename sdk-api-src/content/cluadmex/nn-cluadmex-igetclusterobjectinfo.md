---
UID: NN:cluadmex.IGetClusterObjectInfo
title: IGetClusterObjectInfo
author: windows-sdk-content
description: Called by a Failover Cluster Administrator extension to retrieve information about a cluster object.
old-location: mscs\igetclusterobjectinfo.htm
tech.root: mscs
ms.assetid: a88ba05c-b64b-4d6d-b005-f2f867093355
ms.author: windowssdkdev
ms.date: 08/29/2018
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
 - IGetClusterObjectInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterObjectInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterObjectInfo</b> interface is 
    called by a <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> 
    extension to retrieve information about a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369115(v=VS.85).aspx">cluster object</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterObjectInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IGetClusterObjectInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa370226(v=VS.85).aspx">GetObjectName</a>
</td>
<td align="left" width="63%">
Returns the name of a cluster object.</p> (Inherited from <b>IGetClusterObjectInfo</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370229(v=VS.85).aspx">GetObjectType</a>
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
Failover Cluster Administrator passes in an <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> for one of the 
     <b>IGetClusterObjectInfo</b> methods.

Do not obtain other information interfaces, such as 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterObjectInfo</b> interface. While 
     <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>, 
     and the result is an interface that represents no real cluster object. For an illustration, see 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370230(v=VS.85).aspx">IGetClusterResourceInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369074(v=VS.85).aspx">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370713(v=VS.85).aspx">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370720(v=VS.85).aspx">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370738(v=VS.85).aspx">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370746(v=VS.85).aspx">IWEInvokeCommand::InvokeCommand</a>
 

 

