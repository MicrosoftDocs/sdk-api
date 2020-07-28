---
UID: NF:cluadmex.IWCWizard97Callback.EnableNext
title: IWCWizard97Callback::EnableNext (cluadmex.h)
description: Enables or disables the Next or Finish button on a Wizard97 wizard page, depending on whether the current page is last.
helpviewer_keywords: ["EnableNext","EnableNext method [Failover Cluster]","EnableNext method [Failover Cluster]","IWCWizard97Callback interface","IWCWizard97Callback interface [Failover Cluster]","EnableNext method","IWCWizard97Callback.EnableNext","IWCWizard97Callback::EnableNext","_wolf_iwcwizard97callback_enablenext","cluadmex/IWCWizard97Callback::EnableNext","mscs.iwcwizard97callback_enablenext"]
old-location: mscs\iwcwizard97callback_enablenext.htm
tech.root: MsCS
ms.assetid: aac4dd75-aa98-4db0-8201-33d4c115896b
ms.date: 12/05/2018
ms.keywords: EnableNext, EnableNext method [Failover Cluster], EnableNext method [Failover Cluster],IWCWizard97Callback interface, IWCWizard97Callback interface [Failover Cluster],EnableNext method, IWCWizard97Callback.EnableNext, IWCWizard97Callback::EnableNext, _wolf_iwcwizard97callback_enablenext, cluadmex/IWCWizard97Callback::EnableNext, mscs.iwcwizard97callback_enablenext
f1_keywords:
- cluadmex/IWCWizard97Callback.EnableNext
dev_langs:
- c++
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
- IWCWizard97Callback.EnableNext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWCWizard97Callback::EnableNext


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Enables or disables the <b>Next</b> or <b>Finish</b> button on a 
    Wizard97 wizard page, depending on whether the current page is last.


## -parameters




### -param hpage [in]

Handle to the property page containing the button to be enabled or disabled.


### -param bEnable [in]

Value indicating whether to enable or disable the button. If <i>bEnable</i> is set to 
       <b>TRUE</b>, the appropriate button is enabled. If <i>bEnable</i> is set 
       to <b>FALSE</b>, it is disabled.


## -returns



If <b>EnableNext</b> is not successful, it can return other 
       <b>HRESULT</b> values.

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



Extensions should call the <b>EnableNext</b> 
     method in their handling of the <b>PSN_SETACTIVE</b> message for a property page that 
     they have added to the Failover Cluster Administrator Wizard. 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> determines whether 
     the <b>Next</b> or <b>Finish</b> button should be displayed based on 
     the page specified in the <i>hpage</i> parameter.

For non-Wizard97 pages use 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizardcallback-enablenext">IWCWizardCallback::EnableNext</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizard97callback">IWCWizard97Callback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iwcwizardcallback-enablenext">IWCWizardCallback::EnableNext</a>
 

 

