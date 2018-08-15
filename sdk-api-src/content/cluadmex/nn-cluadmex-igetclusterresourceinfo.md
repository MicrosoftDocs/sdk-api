---
UID: NN:cluadmex.IGetClusterResourceInfo
title: IGetClusterResourceInfo
author: windows-sdk-content
description: Called by a Failover Cluster Administrator extension to retrieve information about a resource.
old-location: mscs\igetclusterresourceinfo.htm
old-project: mscs
ms.assetid: 8a3a9e9d-4666-4d9a-83e3-10d667b42d66
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IGetClusterResourceInfo, IGetClusterResourceInfo interface [Failover Cluster], IGetClusterResourceInfo interface [Failover Cluster],described, _wolf_igetclusterresourceinfo, cluadmex/IGetClusterResourceInfo, mscs.igetclusterresourceinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cluadmex.h
req.include-header: 
req.redist: 
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
 - IGetClusterResourceInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IGetClusterResourceInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterResourceInfo</b> interface is 
    called by a <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> 
    extension to retrieve information about a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterResourceInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetClusterResourceInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetClusterResourceInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a03436da-e12a-45ac-9ac1-1d1896f87fd7">GetResourceHandle</a>
</td>
<td align="left" width="63%">
Returns a handle to a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c4a16ab-b71c-49f6-95cb-8627eaffb8d6">GetResourceNetworkName</a>
</td>
<td align="left" width="63%">
Returns the name of the network managed by the 
      <a href="https://msdn.microsoft.com/7b5b9d3f-98ab-419b-936e-26e9e5fc022d">Network Name</a> resource on which a resource depends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7154163-0ab9-4766-99be-31457a0efc17">GetResourceTypeName</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a> of a resource.

</td>
</tr>
</table> 


## -remarks



If the object being extended is not a resource, queries for 
     <b>IGetClusterResourceInfo</b> methods will fail. 
     Otherwise, you can use the 
     <b>IGetClusterResourceInfo</b> interface when Failover 
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
Failover Cluster Administrator passes in an <a href="_com_iunknown">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="_com_IUnknown_QueryInterface">QueryInterface</a> for one of the 
     <b>IGetClusterResourceInfo</b> methods.

Use the <b>IGetClusterResourceInfo</b> interface only 
     in the context of a resource extension. Do not obtain other information interfaces, such as 
     <a href="https://msdn.microsoft.com/335114ff-3db8-4867-b830-6806adef01f8">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterResourceInfo</b> interface. While 
     <a href="_com_IUnknown_QueryInterface">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the <a href="c_gly.htm">cluster</a>, 
     and the result is an interface that represents no real cluster object.


#### Examples

In the following code, the section enclosed by C-style comments will fail per the previous paragraph.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
// Context is a resource extension.
//
HRESULT CExtObject::HrGetResourceInfo( IGetClusterResourceInfo *piResInfo )
 {
  HRESULT   hr;
  HRESOURCE hRes;
  HGROUP    hGroup;
  HCLUSTER  hCluster;
  DWORD     cchNameSize = MAX_NAME_SIZE; // 256
  WCHAR     szGroupName[cchNameSize];

  IGetClusterGroupInfo *pGrpInfo;

  hRes = piResInfo-&gt;GetResourceHandle();

  //
  // Get group handle
  //
/*******************************************************************
// Incorrect:

  //
  // Obtain an IGetClusterGroupInfo interface from 
  // IGetClusterResourceInfo. By the rules of QueryInterface, this 
  // must return a valid interface. But it is not a valid cluster 
  // operation so the interface won't represent a real object.
  //
  hr = pResInfo-&gt;QueryInterface( IID_IGetClusterGroupInfo, 
                                 (LPVOID *) &amp;pGrpInfo );

  //
  // Interface is valid, will pass this test.
  //
  if( FAILED( hr ) )
    goto Error;

  //
  // FAILS!
  // Interface does not represent a real cluster object.
  //    
  hGrp = pGrpInfo-&gt;GetGroupHandle( 0 );

*******************************************************************/
// Correct:    
  //
  // Use the valid resource handle to call GetClusterResourceState.
  // This yields the name of the group to which it belongs, which
  // can be used to obtain a group handle.
  //
  dwState = GetClusterResourceState( hRes,
                                     NULL,
                                     0,
                                     szGroupName,
                                     &amp;cchGroupNameSize );

  // Add error check.

  hCluster = OpenCluster( g_szClusterName );

  // Add error check.

  hGrp = OpenClusterGroup( hCluster, szGroupName );

  // After error check, use group handle...

 }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3cad771e-5640-4024-8552-d83827fb4e8b">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/48de3627-a919-437b-b19b-374327234df9">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/00eca370-a2c6-4f5c-94a9-7d7e4334ccd5">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/1e723535-d786-496f-bc16-5b10a8a22383">IWEInvokeCommand::InvokeCommand</a>
 

 

