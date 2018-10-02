---
UID: NN:cluadmex.IGetClusterResourceInfo
title: IGetClusterResourceInfo
author: windows-sdk-content
description: Called by a Failover Cluster Administrator extension to retrieve information about a resource.
old-location: mscs\igetclusterresourceinfo.htm
tech.root: MsCS
ms.assetid: 8a3a9e9d-4666-4d9a-83e3-10d667b42d66
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IGetClusterResourceInfo, IGetClusterResourceInfo interface [Failover Cluster], IGetClusterResourceInfo interface [Failover Cluster],described, _wolf_igetclusterresourceinfo, cluadmex/IGetClusterResourceInfo, mscs.igetclusterresourceinfo
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
 - IGetClusterResourceInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetClusterResourceInfo interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterResourceInfo</b> interface is 
    called by a <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> 
    extension to retrieve information about a <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resource</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetClusterResourceInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IGetClusterResourceInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa370231(v=VS.85).aspx">GetResourceHandle</a>
</td>
<td align="left" width="63%">
Returns a handle to a resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370232(v=VS.85).aspx">GetResourceNetworkName</a>
</td>
<td align="left" width="63%">
Returns the name of the network managed by the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa371733(v=VS.85).aspx">Network Name</a> resource on which a resource depends.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370233(v=VS.85).aspx">GetResourceTypeName</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://msdn.microsoft.com/en-us/library/Aa372279(v=VS.85).aspx">resource type</a> of a resource.

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
     <b>IGetClusterResourceInfo</b> methods.

Use the <b>IGetClusterResourceInfo</b> interface only 
     in the context of a resource extension. Do not obtain other information interfaces, such as 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370215(v=VS.85).aspx">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterResourceInfo</b> interface. While 
     <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the <a href="https://msdn.microsoft.com/en-us/library/Aa369336(v=VS.85).aspx">cluster</a>, 
     and the result is an interface that represents no real cluster object.


#### Examples

In the following code, the section enclosed by C-style comments will fail per the previous paragraph.


```cpp
//
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

  hRes = piResInfo->GetResourceHandle();

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
  hr = pResInfo->QueryInterface( IID_IGetClusterGroupInfo, 
                                 (LPVOID *) &pGrpInfo );

  //
  // Interface is valid, will pass this test.
  //
  if( FAILED( hr ) )
    goto Error;

  //
  // FAILS!
  // Interface does not represent a real cluster object.
  //    
  hGrp = pGrpInfo->GetGroupHandle( 0 );

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
                                     &cchGroupNameSize );

  // Add error check.

  hCluster = OpenCluster( g_szClusterName );

  // Add error check.

  hGrp = OpenClusterGroup( hCluster, szGroupName );

  // After error check, use group handle...

 }

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369074(v=VS.85).aspx">Failover Cluster Administrator Information Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370713(v=VS.85).aspx">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370720(v=VS.85).aspx">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370738(v=VS.85).aspx">IWEExtendWizard::CreateWizardPages</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370746(v=VS.85).aspx">IWEInvokeCommand::InvokeCommand</a>
 

 

