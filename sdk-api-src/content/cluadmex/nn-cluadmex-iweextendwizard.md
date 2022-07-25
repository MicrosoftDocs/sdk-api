---
UID: NN:cluadmex.IWEExtendWizard
title: IWEExtendWizard (cluadmex.h)
description: Implement the IWEExtendWizard interface to add wizard pages to Failover Cluster Administrator's New Resource Wizard or Cluster Application Wizard.
helpviewer_keywords: ["IWEExtendWizard","IWEExtendWizard interface [Failover Cluster]","IWEExtendWizard interface [Failover Cluster]","described","_wolf_iweextendwizard","cluadmex/IWEExtendWizard","mscs.iweextendwizard"]
old-location: mscs\iweextendwizard.htm
tech.root: MsCS
ms.assetid: 6407163e-a8ca-4601-88a0-ecf87e29b9ab
ms.date: 12/05/2018
ms.keywords: IWEExtendWizard, IWEExtendWizard interface [Failover Cluster], IWEExtendWizard interface [Failover Cluster],described, _wolf_iweextendwizard, cluadmex/IWEExtendWizard, mscs.iweextendwizard
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
 - IWEExtendWizard
 - cluadmex/IWEExtendWizard
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
 - IWEExtendWizard
---

# IWEExtendWizard interface


## -description

<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Implement the <b>IWEExtendWizard</b> interface to 
    add wizard pages to <a href="/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator's</a> 
    New Resource Wizard or Cluster Application Wizard.

## -inheritance

The <b>IWEExtendWizard</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEExtendWizard</b> also has these types of members:

## -remarks

To support Wizard97 wizards and wizard pages, implement the 
     <a href="/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard97">IWEExtendWizard97</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>
