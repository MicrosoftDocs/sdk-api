---
UID: NF:cluadmex.IWEExtendWizard97.CreateWizard97Pages
title: IWEExtendWizard97::CreateWizard97Pages (cluadmex.h)
description: Allows you to create Wizard97 property pages and add them to a Failover Cluster Administrator Wizard.
helpviewer_keywords: ["CreateWizard97Pages","CreateWizard97Pages method [Failover Cluster]","CreateWizard97Pages method [Failover Cluster]","IWEExtendWizard97 interface","IWEExtendWizard97 interface [Failover Cluster]","CreateWizard97Pages method","IWEExtendWizard97.CreateWizard97Pages","IWEExtendWizard97::CreateWizard97Pages","_wolf_iweextendwizard97_createwizard97pages","cluadmex/IWEExtendWizard97::CreateWizard97Pages","mscs.iweextendwizard97_createwizard97pages"]
old-location: mscs\iweextendwizard97_createwizard97pages.htm
tech.root: MsCS
ms.assetid: 1ab81008-42d8-4863-8836-0508e49ceca9
ms.date: 12/05/2018
ms.keywords: CreateWizard97Pages, CreateWizard97Pages method [Failover Cluster], CreateWizard97Pages method [Failover Cluster],IWEExtendWizard97 interface, IWEExtendWizard97 interface [Failover Cluster],CreateWizard97Pages method, IWEExtendWizard97.CreateWizard97Pages, IWEExtendWizard97::CreateWizard97Pages, _wolf_iweextendwizard97_createwizard97pages, cluadmex/IWEExtendWizard97::CreateWizard97Pages, mscs.iweextendwizard97_createwizard97pages
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
 - IWEExtendWizard97::CreateWizard97Pages
 - cluadmex/IWEExtendWizard97::CreateWizard97Pages
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
 - IWEExtendWizard97.CreateWizard97Pages
---

# IWEExtendWizard97::CreateWizard97Pages


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Allows you to create Wizard97 property pages and add them to a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> Wizard.

## -parameters

### -param piData [in]

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer for retrieving information 
       relating to the wizard97 pages to be added. By calling 
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
Depending on the type of <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster object</a>, a 
       pointer to one of the following interfaces is also available:

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

Pointer to an <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizard97callback">IWCWizard97Callback</a> interface 
       implementation used to add the new Wizard97 property pages to the wizard.

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
The extension does not support adding Wizard97 pages.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your extension has no Wizard97 pages but does have non-Wizard97 pages, you can either:

<ul>
<li>Support only the <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard">IWEExtendWizard</a> interface.</li>
<li>Support both the <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard">IWEExtendWizard</a> and 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard97">IWEExtendWizard97</a> interfaces, but in your 
       implementation of <b>IWEExtendWizard97</b>, query for the 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizardcallback">IWCWizardCallback</a> interface from the interface 
       passed in by way of the <i>piCallback</i> parameter.</li>
</ul>
<p class="proch"><b>For each Wizard97 property page to be added</b>

<ol>
<li>Use <i>piData</i> to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> and retrieve an 
       interface pointer for the <a href="/previous-versions/windows/desktop/mscs/cluster-objects">object</a> associated with the new 
       page. For example, if you are adding a property page for a resource, you want to retrieve a pointer to the 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the object being 
       extended, you should expect to receive errors when you attempt to call the methods.</li>
<li>To create the page, call the function 
       <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new wizard97 page should be no larger than 293 
       dialog units wide and 172 dialog units high, and should contain a static control positioned at (38,12) with a 
       size of (247,10).</li>
<li>To add the page to a Cluster Administrator Wizard, call 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizard97callback-addwizard97page">IWCWizard97Callback::AddWizard97Page</a> 
       using the <i>piCallback</i> pointer.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>



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