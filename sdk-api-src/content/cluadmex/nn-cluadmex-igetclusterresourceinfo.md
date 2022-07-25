---
UID: NN:cluadmex.IGetClusterResourceInfo
title: IGetClusterResourceInfo (cluadmex.h)
description: Called by a Failover Cluster Administrator extension to retrieve information about a resource.
helpviewer_keywords: ["IGetClusterResourceInfo","IGetClusterResourceInfo interface [Failover Cluster]","IGetClusterResourceInfo interface [Failover Cluster]","described","_wolf_igetclusterresourceinfo","cluadmex/IGetClusterResourceInfo","mscs.igetclusterresourceinfo"]
old-location: mscs\igetclusterresourceinfo.htm
tech.root: MsCS
ms.assetid: 8a3a9e9d-4666-4d9a-83e3-10d667b42d66
ms.date: 12/05/2018
ms.keywords: IGetClusterResourceInfo, IGetClusterResourceInfo interface [Failover Cluster], IGetClusterResourceInfo interface [Failover Cluster],described, _wolf_igetclusterresourceinfo, cluadmex/IGetClusterResourceInfo, mscs.igetclusterresourceinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetClusterResourceInfo
 - cluadmex/IGetClusterResourceInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IGetClusterResourceInfo
---

# IGetClusterResourceInfo interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IGetClusterResourceInfo</b> interface is 
    called by a <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> 
    extension to retrieve information about a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>.

## -inheritance

The <b>IGetClusterResourceInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGetClusterResourceInfo</b> also has these types of members:

## -remarks

If the object being extended is not a resource, queries for 
     <b>IGetClusterResourceInfo</b> methods will fail. 
     Otherwise, you can use the 
     <b>IGetClusterResourceInfo</b> interface when Failover 
     Cluster Administrator calls your implementations of the following methods:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
</li>
</ul>
Failover Cluster Administrator passes in an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer, 
     <i>piData</i>. Use <i>piData</i> to call 
     <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for one of the 
     <b>IGetClusterResourceInfo</b> methods.

Use the <b>IGetClusterResourceInfo</b> interface only 
     in the context of a resource extension. Do not obtain other information interfaces, such as 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>, from the 
     <b>IGetClusterResourceInfo</b> interface. While 
     <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> will return a valid interface, 
     the operation is not valid in the context of the <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster</a>, 
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

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-information-interfaces">Failover Cluster Administrator Information Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendcontextmenu-addcontextmenuitems">IWEExtendContextMenu::AddContextMenuItems</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweinvokecommand-invokecommand">IWEInvokeCommand::InvokeCommand</a>
