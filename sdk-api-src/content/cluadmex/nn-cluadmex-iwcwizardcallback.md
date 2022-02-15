---
UID: NN:cluadmex.IWCWizardCallback
title: IWCWizardCallback (cluadmex.h)
description: The IWCWizardCallback interface is called by a Failover Cluster Administrator extension to add a property page to a Failover Cluster Administrator Wizard and to manage navigation.
helpviewer_keywords: ["IWCWizardCallback","IWCWizardCallback interface [Failover Cluster]","IWCWizardCallback interface [Failover Cluster]","described","_wolf_iwcwizardcallback","cluadmex/IWCWizardCallback","mscs.iwcwizardcallback"]
old-location: mscs\iwcwizardcallback.htm
tech.root: MsCS
ms.assetid: 0d5f45c4-6091-4ea4-875a-69be7f1258db
ms.date: 12/05/2018
ms.keywords: IWCWizardCallback, IWCWizardCallback interface [Failover Cluster], IWCWizardCallback interface [Failover Cluster],described, _wolf_iwcwizardcallback, cluadmex/IWCWizardCallback, mscs.iwcwizardcallback
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
 - IWCWizardCallback
 - cluadmex/IWCWizardCallback
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
 - IWCWizardCallback
---

# IWCWizardCallback interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IWCWizardCallback</b> interface is called by a 
    <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator</a> extension to add a 
    property page to a Failover Cluster Administrator Wizard and to manage navigation.

## -inheritance

The <b>IWCWizardCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWCWizardCallback</b> also has these types of members:

## -remarks

Use the <i>piCallback</i> pointer that you receive when Failover Cluster Administrator calls 
     your 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a> 
     method to call the methods of the <b>IWCWizardCallback</b> 
     interface.

Use <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizard97callback">IWCWizard97Callback</a> to add Wizard97 pages.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-callback-interfaces">Failover Cluster Administrator Callback Interfaces</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iwcwizard97callback">IWCWizard97Callback</a>



<a href="/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">IWEExtendWizard::CreateWizardPages</a>
