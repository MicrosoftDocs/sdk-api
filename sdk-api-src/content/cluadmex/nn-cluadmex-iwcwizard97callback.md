---
UID: NN:cluadmex.IWCWizard97Callback
title: IWCWizard97Callback (cluadmex.h)
description: The IWCWizard97Callback interface is called by a Failover Cluster Administrator extension to add a Wizard97 property page to a Wizard97 wizard, such as the Cluster Application Wizard.
helpviewer_keywords: ["IWCWizard97Callback","IWCWizard97Callback interface [Failover Cluster]","IWCWizard97Callback interface [Failover Cluster]","described","_wolf_iwcwizard97callback","cluadmex/IWCWizard97Callback","mscs.iwcwizard97callback"]
old-location: mscs\iwcwizard97callback.htm
tech.root: MsCS
ms.assetid: cbde3bcf-8242-49dc-9ac0-a4b078ea526e
ms.date: 12/05/2018
ms.keywords: IWCWizard97Callback, IWCWizard97Callback interface [Failover Cluster], IWCWizard97Callback interface [Failover Cluster],described, _wolf_iwcwizard97callback, cluadmex/IWCWizard97Callback, mscs.iwcwizard97callback
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
 - IWCWizard97Callback
 - cluadmex/IWCWizard97Callback
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
 - IWCWizard97Callback
---

# IWCWizard97Callback interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IWCWizard97Callback</b> interface is called by a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extension to add a 
    Wizard97 property page to a Wizard97 wizard, such as the Cluster Application Wizard.

## -inheritance

The <b>IWCWizard97Callback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWCWizard97Callback</b> also has these types of members:

## -remarks

Use the piCallback pointer that you receive when Cluster Administrator calls your 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a> 
     method to call the methods of the 
     <b>IWCWizard97Callback</b> interface.

To add non-Wizard97 pages use <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizardcallback">IWCWizardCallback</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-callback-interfaces">Failover Cluster Administrator Callback Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizardcallback">IWCWizardCallback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard97-createwizard97pages">IWEExtendWizard97::CreateWizard97Pages</a>
