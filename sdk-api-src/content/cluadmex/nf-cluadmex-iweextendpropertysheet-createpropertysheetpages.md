---
UID: NF:cluadmex.IWEExtendPropertySheet.CreatePropertySheetPages
title: IWEExtendPropertySheet::CreatePropertySheetPages (cluadmex.h)
description: Creates property pages for a cluster object and adds them to a Failover Cluster Administrator property sheet.
helpviewer_keywords: ["CreatePropertySheetPages","CreatePropertySheetPages method [Failover Cluster]","CreatePropertySheetPages method [Failover Cluster]","IWEExtendPropertySheet interface","IWEExtendPropertySheet interface [Failover Cluster]","CreatePropertySheetPages method","IWEExtendPropertySheet.CreatePropertySheetPages","IWEExtendPropertySheet::CreatePropertySheetPages","_wolf_iweextendpropertysheet_createpropertysheetpages","cluadmex/IWEExtendPropertySheet::CreatePropertySheetPages","mscs.iweextendpropertysheet_createpropertysheetpages"]
old-location: mscs\iweextendpropertysheet_createpropertysheetpages.htm
tech.root: MsCS
ms.assetid: 00eca370-a2c6-4f5c-94a9-7d7e4334ccd5
ms.date: 12/05/2018
ms.keywords: CreatePropertySheetPages, CreatePropertySheetPages method [Failover Cluster], CreatePropertySheetPages method [Failover Cluster],IWEExtendPropertySheet interface, IWEExtendPropertySheet interface [Failover Cluster],CreatePropertySheetPages method, IWEExtendPropertySheet.CreatePropertySheetPages, IWEExtendPropertySheet::CreatePropertySheetPages, _wolf_iweextendpropertysheet_createpropertysheetpages, cluadmex/IWEExtendPropertySheet::CreatePropertySheetPages, mscs.iweextendpropertysheet_createpropertysheetpages
req.header: cluadmex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - IWEExtendPropertySheet::CreatePropertySheetPages
 - cluadmex/IWEExtendPropertySheet::CreatePropertySheetPages
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
 - IWEExtendPropertySheet.CreatePropertySheetPages
---

# IWEExtendPropertySheet::CreatePropertySheetPages


## -description

Creates property pages for a <a href="/previous-versions/windows/desktop/mscs/c-gly">cluster object</a> and 
    adds them to a <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> 
    property sheet.

## -parameters

### -param piData [in]

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer for retrieving information relating to the new 
       property pages. By calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method with the 
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
       which property sheet pages are being created, a pointer to one of the following interfaces is also 
       available:

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

Pointer to an <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcpropertysheetcallback">IWCPropertySheetCallback</a> 
       interface implementation for adding property pages to the Cluster Administrator property sheet.

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
The extension does not support adding property pages.

</td>
</tr>
</table>

## -remarks

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> calls 
     an extension's 
     <b>CreatePropertySheetPages</b> 
     method to extend a property sheet to handle an additional 
     <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster object</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<p class="proch"><b>For each property page to be added</b>

<ol>
<li>Use <i>piData</i> to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> and retrieve an 
       interface pointer for the cluster object associated with the page. For example, if you are adding a property 
       page for a resource, you want to retrieve a pointer to the 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-igetclusterresourceinfo">IGetClusterResourceInfo</a> interface. 
       Although it is possible to successfully query for interfaces that retrieve data unrelated to the target object, 
       you should expect to receive errors when you attempt to call the methods.</li>
<li>
To create the page, call the function 
       <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a>. To produce pages 
       that look like the pages provided by Cluster Administrator, each new property page should be no larger than 252 
       dialog units wide and 218 dialog units high, and should contain two standard controls:

<ul>
<li>For the object icon, an icon control positioned at (8,7) with a size of (18,20).</li>
<li>For the object name, a static control positioned at (38,12) with a size of (206,10).</li>
</ul>
</li>
<li>To add the page to the property sheet, call the 
       <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcpropertysheetcallback-addpropertysheetpage">IWCPropertySheetCallback::AddPropertySheetPage</a> 
       method pointed to by <i>piCallback</i>.</li>
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



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcpropertysheetcallback">IWCPropertySheetCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcpropertysheetcallback-addpropertysheetpage">IWCPropertySheetCallback::AddPropertySheetPage</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendpropertysheet">IWEExtendPropertySheet</a>