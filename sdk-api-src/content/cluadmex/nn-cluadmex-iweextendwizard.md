---
UID: NN:cluadmex.IWEExtendWizard
title: IWEExtendWizard (cluadmex.h)
author: windows-sdk-content
description: Implement the IWEExtendWizard interface to add wizard pages to Failover Cluster Administrator's New Resource Wizard or Cluster Application Wizard.
old-location: mscs\iweextendwizard.htm
tech.root: MsCS
ms.assetid: 6407163e-a8ca-4601-88a0-ecf87e29b9ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWEExtendWizard, IWEExtendWizard interface [Failover Cluster], IWEExtendWizard interface [Failover Cluster],described, _wolf_iweextendwizard, cluadmex/IWEExtendWizard, mscs.iweextendwizard
ms.topic: interface
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
 - IWEExtendWizard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWEExtendWizard interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

Implement the <b>IWEExtendWizard</b> interface to 
    add wizard pages to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator">Failover Cluster Administrator's</a> 
    New Resource Wizard or Cluster Application Wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWEExtendWizard</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWEExtendWizard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWEExtendWizard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nf-cluadmex-iweextendwizard-createwizardpages">CreateWizardPages</a>
</td>
<td align="left" width="63%">
Allows you to create wizard pages and add them to Failover Cluster Administrator's New Resource Wizard or 
      Cluster Application Wizard.

</td>
</tr>
</table> 


## -remarks



To support Wizard97 wizards and wizard pages, implement the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cluadmex/nn-cluadmex-iweextendwizard97">IWEExtendWizard97</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-administrator-extension-interfaces">Failover Cluster Administrator Extension Interfaces</a>
 

 

