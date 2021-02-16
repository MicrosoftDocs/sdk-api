---
UID: NF:cluadmex.IWCPropertySheetCallback.AddPropertySheetPage
title: IWCPropertySheetCallback::AddPropertySheetPage (cluadmex.h)
description: Adds a property page to a Failover Cluster Administrator property sheet.
helpviewer_keywords: ["AddPropertySheetPage","AddPropertySheetPage method [Failover Cluster]","AddPropertySheetPage method [Failover Cluster]","IWCPropertySheetCallback interface","IWCPropertySheetCallback interface [Failover Cluster]","AddPropertySheetPage method","IWCPropertySheetCallback.AddPropertySheetPage","IWCPropertySheetCallback::AddPropertySheetPage","_wolf_iwcpropertysheetcallback_addpropertysheetpage","cluadmex/IWCPropertySheetCallback::AddPropertySheetPage","mscs.iwcpropertysheetcallback_addpropertysheetpage"]
old-location: mscs\iwcpropertysheetcallback_addpropertysheetpage.htm
tech.root: MsCS
ms.assetid: ccd87d3a-c9da-4d61-9e9b-f25a52724166
ms.date: 12/05/2018
ms.keywords: AddPropertySheetPage, AddPropertySheetPage method [Failover Cluster], AddPropertySheetPage method [Failover Cluster],IWCPropertySheetCallback interface, IWCPropertySheetCallback interface [Failover Cluster],AddPropertySheetPage method, IWCPropertySheetCallback.AddPropertySheetPage, IWCPropertySheetCallback::AddPropertySheetPage, _wolf_iwcpropertysheetcallback_addpropertysheetpage, cluadmex/IWCPropertySheetCallback::AddPropertySheetPage, mscs.iwcpropertysheetcallback_addpropertysheetpage
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
 - IWCPropertySheetCallback::AddPropertySheetPage
 - cluadmex/IWCPropertySheetCallback::AddPropertySheetPage
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
 - IWCPropertySheetCallback.AddPropertySheetPage
---

# IWCPropertySheetCallback::AddPropertySheetPage


## -description

Adds a property page to a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> property sheet.

## -parameters

### -param hpage [in]

Handle to the property page to be added.

## -returns

If 
       <b>AddPropertySheetPage</b> 
       was not successful, it can return other <b>HRESULT</b> values.

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
The <i>hpage</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

Call the 
     <b>AddPropertySheetPage</b> 
     method from your 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a> 
     implementation. However, before you call 
     <b>AddPropertySheetPage</b>, 
     call the function <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> 
     to retrieve a handle to pass in the <i>hpage</i> parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcpropertysheetcallback">IWCPropertySheetCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendpropertysheet-createpropertysheetpages">IWEExtendPropertySheet::CreatePropertySheetPages</a>