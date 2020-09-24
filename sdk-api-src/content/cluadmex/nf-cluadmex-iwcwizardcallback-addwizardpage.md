---
UID: NF:cluadmex.IWCWizardCallback.AddWizardPage
title: IWCWizardCallback::AddWizardPage (cluadmex.h)
description: Adds a property page to a Failover Cluster Administrator Wizard.
helpviewer_keywords: ["AddWizardPage","AddWizardPage method [Failover Cluster]","AddWizardPage method [Failover Cluster]","IWCWizardCallback interface","IWCWizardCallback interface [Failover Cluster]","AddWizardPage method","IWCWizardCallback.AddWizardPage","IWCWizardCallback::AddWizardPage","_wolf_iwcwizardcallback_addwizardpage","cluadmex/IWCWizardCallback::AddWizardPage","mscs.iwcwizardcallback_addwizardpage"]
old-location: mscs\iwcwizardcallback_addwizardpage.htm
tech.root: MsCS
ms.assetid: e5ce7798-c1e6-47b6-a1bf-1262b3511b22
ms.date: 12/05/2018
ms.keywords: AddWizardPage, AddWizardPage method [Failover Cluster], AddWizardPage method [Failover Cluster],IWCWizardCallback interface, IWCWizardCallback interface [Failover Cluster],AddWizardPage method, IWCWizardCallback.AddWizardPage, IWCWizardCallback::AddWizardPage, _wolf_iwcwizardcallback_addwizardpage, cluadmex/IWCWizardCallback::AddWizardPage, mscs.iwcwizardcallback_addwizardpage
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
 - IWCWizardCallback::AddWizardPage
 - cluadmex/IWCWizardCallback::AddWizardPage
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
 - IWCWizardCallback.AddWizardPage
---

# IWCWizardCallback::AddWizardPage


## -description

<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Adds a property page to a Failover Cluster Administrator Wizard.

## -parameters

### -param hpage [in]

Handle to the property page to be added.

## -returns

If <b>AddWizardPage</b> is not successful, 
       it can return other <b>HRESULT</b> values.

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
     <b>AddWizardPage</b> method from their 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a> 
     methods. Before calling <b>AddWizardPage</b>, 
     extensions must call the function 
     <a href="/windows/desktop/api/prsht/nf-prsht-createpropertysheetpagea">CreatePropertySheetPage</a> to retrieve a 
     handle to pass in the <i>hpage</i> parameter.

Use 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizard97callback-addwizard97page">IWCWizard97Calllback::AddWizard97Page</a> 
     to add Wizard97 pages.

## -see-also

<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizard97callback-addwizard97page">IWCWizard97Callback::AddWizard97Page</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizardcallback">IWCWizardCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>