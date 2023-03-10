---
UID: NF:cluadmex.IWEExtendWizard.CreateWizardPages
title: IWEExtendWizard::CreateWizardPages (cluadmex.h)
description: Allows you to create wizard pages and add them to Failover Cluster Administrator's New Resource Wizard or Cluster Application Wizard.
helpviewer_keywords: ["CreateWizardPages","CreateWizardPages method [Failover Cluster]","CreateWizardPages method [Failover Cluster]","IWEExtendWizard interface","IWEExtendWizard interface [Failover Cluster]","CreateWizardPages method","IWEExtendWizard.CreateWizardPages","IWEExtendWizard::CreateWizardPages","_wolf_iweextendwizard_createwizardpages","cluadmex/IWEExtendWizard::CreateWizardPages","mscs.iweextendwizard_createwizardpages"]
old-location: mscs\iweextendwizard_createwizardpages.htm
tech.root: MsCS
ms.assetid: b52ea5a5-aa80-4f65-9bab-b60fa8363b01
ms.date: 12/05/2018
ms.keywords: CreateWizardPages, CreateWizardPages method [Failover Cluster], CreateWizardPages method [Failover Cluster],IWEExtendWizard interface, IWEExtendWizard interface [Failover Cluster],CreateWizardPages method, IWEExtendWizard.CreateWizardPages, IWEExtendWizard::CreateWizardPages, _wolf_iweextendwizard_createwizardpages, cluadmex/IWEExtendWizard::CreateWizardPages, mscs.iweextendwizard_createwizardpages
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
 - IWEExtendWizard::CreateWizardPages
 - cluadmex/IWEExtendWizard::CreateWizardPages
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
 - IWEExtendWizard.CreateWizardPages
---

# IWEExtendWizard::CreateWizardPages


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create wizard pages and add them to 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator's</a> New Resource Wizard 
     or Cluster Application Wizard.

## -parameters

### -param piData [in]

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer for retrieving information 
       relating to the wizard pages to be added. By calling 
       <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> with the 
       <i>piData</i> pointer, the following interfaces are available:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterdatainfo">IGetClusterDataInfo</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterobjectinfo">IGetClusterObjectInfo</a>
</li>
</ul>
Depending on the type of <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster object</a> for 
       which the wizard page is being created, a pointer to one of the following interfaces is also available:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternodeinfo">IGetClusterNodeInfo</a>, if the property page 
        relates to a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>, if the property page 
        relates to a <a href="/previous-versions/windows/desktop/mscs/groups">group</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetworkinfo">IGetClusterNetworkInfo</a>, if the property 
        page relates to a <a href="/previous-versions/windows/desktop/mscs/networks">network</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetinterfaceinfo">IGetClusterNetInterfaceInfo</a>, if the 
        property page relates to a <a href="/previous-versions/windows/desktop/mscs/network-interfaces">network interface</a>.</li>
<li>
<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>, if the property 
        page relates to a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>.</li>
</ul>

### -param piCallback [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizardcallback">IWCWizardCallback</a> interface 
       implementation used to add the new property pages to the wizard.

## -returns

Return one of the following values or any <b>HRESULT</b> that describes the results of 
       the operation.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NOERROR</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
At least one of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
<dt>0x80004001</dt>
</dl>
</td>
<td width="60%">
The extension does not support adding a property page to the Create Group Wizard or Create Resource 
         Wizard.

</td>
</tr>
</table>

## -remarks

To add Wizard97 wizard pages, use the 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a> 
     method.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<p class="proch"><b>For each property page to be added</b>

<ol>
<li>Use <i>piData</i> to call 
       <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> and retrieve an interface 
       pointer for the <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a> associated with the new 
       page. For example, if you are adding a property page for a resource, you want to retrieve a pointer to the 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the object being 
       extended, you should expect to receive errors when you attempt to call the methods.</li>
<li>
To create the page, call the function 
       <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new property page should be no larger than 252 
       dialog units wide and 218 dialog units high, and should contain two standard controls:

<ul>
<li>For the object icon, an icon control positioned at (8,7) with a size of (18,20).</li>
<li>For the object name, a static control positioned at (38,12) with a size of (247,10).</li>
</ul>
</li>
<li>To add the page to a Cluster Administrator Wizard, call 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizardcallback-addwizardpage">IWCWizardCallback::AddWizardPage</a> 
       using the <i>piCallback</i> pointer.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterdatainfo">IGetClusterDataInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclustergroupinfo">IGetClusterGroupInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetinterfaceinfo">IGetClusterNetInterfaceInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternetworkinfo">IGetClusterNetworkInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusternodeinfo">IGetClusterNodeInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterobjectinfo">IGetClusterObjectInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusteruiinfo">IGetClusterUIInfo</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcpropertysheetcallback-addpropertysheetpage">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizardcallback">IWCWizardCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard">IWEExtendWizard</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard97">IWEExtendWizard97</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>