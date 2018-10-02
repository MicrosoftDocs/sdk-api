---
UID: NN:cluadmex.IWCWizardCallback
title: IWCWizardCallback
author: windows-sdk-content
description: The IWCWizardCallback interface is called by a Failover Cluster Administrator extension to add a property page to a Failover Cluster Administrator Wizard and to manage navigation.
old-location: mscs\iwcwizardcallback.htm
tech.root: MsCS
ms.assetid: 0d5f45c4-6091-4ea4-875a-69be7f1258db
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWCWizardCallback, IWCWizardCallback interface [Failover Cluster], IWCWizardCallback interface [Failover Cluster],described, _wolf_iwcwizardcallback, cluadmex/IWCWizardCallback, mscs.iwcwizardcallback
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
 - IWCWizardCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCWizardCallback interface


## -description


<p class="CCE_Message">[This interface is available for use in the operating systems specified in the Requirements 
    section. Support for this interface was removed in Windows Server 2008.]

The <b>IWCWizardCallback</b> interface is called by a 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extension to add a 
    property page to a Failover Cluster Administrator Wizard and to manage navigation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWCWizardCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWCWizardCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWCWizardCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5ce7798-c1e6-47b6-a1bf-1262b3511b22">AddWizardPage</a>
</td>
<td align="left" width="63%">
Adds a property page to a Failover Cluster Administrator Wizard.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f485ffa-0e94-4443-9c79-991c35a60e97">EnableNext</a>
</td>
<td align="left" width="63%">
Enables or disables the <b>Next</b> or <b>Finish</b> button on a 
      Failover Cluster Administrator Wizard page, depending on whether the current page is last.

</td>
</tr>
</table> 


## -remarks



Use the <i>piCallback</i> pointer that you receive when Failover Cluster Administrator calls 
     your 
     <a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a> 
     method to call the methods of the <b>IWCWizardCallback</b> 
     interface.

Use <a href="https://msdn.microsoft.com/cbde3bcf-8242-49dc-9ac0-a4b078ea526e">IWCWizard97Callback</a> to add Wizard97 pages.




## -see-also




<a href="https://msdn.microsoft.com/4a2b0c21-1b3f-4037-a143-02956e6996ce">Failover Cluster Administrator Callback Interfaces</a>



<a href="https://msdn.microsoft.com/cbde3bcf-8242-49dc-9ac0-a4b078ea526e">IWCWizard97Callback</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>
 

 

