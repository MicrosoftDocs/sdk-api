---
UID: NF:cluadmex.IWCWizardCallback.AddWizardPage
title: IWCWizardCallback::AddWizardPage method
author: windows-driver-content
description: Adds a property page to a Failover Cluster Administrator Wizard.
old-location: mscs\iwcwizardcallback_addwizardpage.htm
old-project: MsCS
ms.assetid: e5ce7798-c1e6-47b6-a1bf-1262b3511b22
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: AddWizardPage method [Failover Cluster], AddWizardPage method [Failover Cluster], IWCWizardCallback interface, AddWizardPage,IWCWizardCallback.AddWizardPage, IWCWizardCallback, IWCWizardCallback interface [Failover Cluster], AddWizardPage method, IWCWizardCallback::AddWizardPage, _wolf_iwcwizardcallback_addwizardpage, cluadmex/IWCWizardCallback::AddWizardPage, mscs.iwcwizardcallback_addwizardpage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	cluadmex.h
api_name:
-	IWCWizardCallback.AddWizardPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IWCWizardCallback::AddWizardPage method


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




## -remarks




<a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extensions call the 
     <b>AddWizardPage</b> method from their 
     <a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a> 
     methods. Before calling <b>AddWizardPage</b>, 
     extensions must call the function 
     <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a> to retrieve a 
     handle to pass in the <i>hpage</i> parameter.

Use 
     <a href="https://msdn.microsoft.com/c5de70da-2a08-4142-8f21-53a98e28fd42">IWCWizard97Calllback::AddWizard97Page</a> 
     to add Wizard97 pages.




## -see-also




<a href="https://msdn.microsoft.com/c5de70da-2a08-4142-8f21-53a98e28fd42">IWCWizard97Callback::AddWizard97Page</a>



<a href="https://msdn.microsoft.com/0d5f45c4-6091-4ea4-875a-69be7f1258db">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/b52ea5a5-aa80-4f65-9bab-b60fa8363b01">IWEExtendWizard::CreateWizardPages</a>
 

 

