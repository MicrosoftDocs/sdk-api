---
UID: NF:cluadmex.IWCWizard97Callback.AddWizard97Page
title: IWCWizard97Callback::AddWizard97Page (cluadmex.h)
description: Adds a Wizard97 property page to a Wizard97 wizard, such as the Failover Cluster Application Wizard.
helpviewer_keywords: ["AddWizard97Page","AddWizard97Page method [Failover Cluster]","AddWizard97Page method [Failover Cluster]","IWCWizard97Callback interface","IWCWizard97Callback interface [Failover Cluster]","AddWizard97Page method","IWCWizard97Callback.AddWizard97Page","IWCWizard97Callback::AddWizard97Page","_wolf_iwcwizard97callback_addwizard97page","cluadmex/IWCWizard97Callback::AddWizard97Page","mscs.iwcwizard97callback_addwizard97page"]
old-location: mscs\iwcwizard97callback_addwizard97page.htm
tech.root: MsCS
ms.assetid: c5de70da-2a08-4142-8f21-53a98e28fd42
ms.date: 12/05/2018
ms.keywords: AddWizard97Page, AddWizard97Page method [Failover Cluster], AddWizard97Page method [Failover Cluster],IWCWizard97Callback interface, IWCWizard97Callback interface [Failover Cluster],AddWizard97Page method, IWCWizard97Callback.AddWizard97Page, IWCWizard97Callback::AddWizard97Page, _wolf_iwcwizard97callback_addwizard97page, cluadmex/IWCWizard97Callback::AddWizard97Page, mscs.iwcwizard97callback_addwizard97page
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
 - IWCWizard97Callback::AddWizard97Page
 - cluadmex/IWCWizard97Callback::AddWizard97Page
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
 - IWCWizard97Callback.AddWizard97Page
---

# IWCWizard97Callback::AddWizard97Page


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Adds a Wizard97 property page to a Wizard97 wizard, such as the Failover Cluster Application Wizard.

## -parameters

### -param hpage [in]

Handle to the property page to be added.

## -returns

If <b>AddWizard97Page</b> is not 
       successful, it can return other <b>HRESULT</b> values.

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
The <i>hpage</i> parameter represents an unknown page.

</td>
</tr>
</table>

## -remarks

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extensions call the 
     <b>AddWizard97Page</b> method from their 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a> 
     methods. Before calling 
     <b>AddWizard97Page</b>, extensions must 
     call the function <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> 
     to retrieve a handle to pass in the <i>hpage</i> parameter.

To add non-Wizard97 pages, use 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizardcallback-addwizardpage">IWCWizardCallback::AddWizardPage</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizard97callback">IWCWizard97Callback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizardcallback-addwizardpage">IWCWizardCallback::AddWizardPage</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>