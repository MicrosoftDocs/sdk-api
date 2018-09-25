---
UID: NN:cluadmex.IWCWizard97Callback
title: IWCWizard97Callback
author: windows-sdk-content
description: The IWCWizard97Callback interface is called by a Failover Cluster Administrator extension to add a Wizard97 property page to a Wizard97 wizard, such as the Cluster Application Wizard.
old-location: mscs\iwcwizard97callback.htm
tech.root: mscs
ms.assetid: cbde3bcf-8242-49dc-9ac0-a4b078ea526e
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IWCWizard97Callback, IWCWizard97Callback interface [Failover Cluster], IWCWizard97Callback interface [Failover Cluster],described, _wolf_iwcwizard97callback, cluadmex/IWCWizard97Callback, mscs.iwcwizard97callback
ms.prod: windows
ms.technology: windows-sdk
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
 - IWCWizard97Callback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCWizard97Callback interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IWCWizard97Callback</b> interface is called by a 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> extension to add a 
    Wizard97 property page to a Wizard97 wizard, such as the Cluster Application Wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCWizard97Callback</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IWCWizard97Callback</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IWCWizard97Callback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370512(v=VS.85).aspx">AddWizard97Page</a>
</td>
<td align="left" width="63%">
Adds a property page to a Wizard97 wizard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa370515(v=VS.85).aspx">EnableNext</a>
</td>
<td align="left" width="63%">
Enables or disables the <b>Next</b> or <b>Finish</b> button on a 
      Wizard97 page, depending on whether the current page is last.

</td>
</tr>
</table> 


## -remarks



Use the piCallback pointer that you receive when Cluster Administrator calls your 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a> 
     method to call the methods of the 
     <b>IWCWizard97Callback</b> interface.

To add non-Wizard97 pages use <a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369061(v=VS.85).aspx">Failover Cluster Administrator Callback Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370733(v=VS.85).aspx">IWEExtendWizard97::CreateWizard97Pages</a>
 

 

