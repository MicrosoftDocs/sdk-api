---
UID: NF:cluadmex.IWCWizardCallback.AddWizardPage
title: IWCWizardCallback::AddWizardPage
author: windows-sdk-content
description: Adds a property page to a Failover Cluster Administrator Wizard.
old-location: mscs\iwcwizardcallback_addwizardpage.htm
old-project: mscs
ms.assetid: e5ce7798-c1e6-47b6-a1bf-1262b3511b22
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddWizardPage, AddWizardPage method [Failover Cluster], AddWizardPage method [Failover Cluster],IWCWizardCallback interface, IWCWizardCallback interface [Failover Cluster],AddWizardPage method, IWCWizardCallback.AddWizardPage, IWCWizardCallback::AddWizardPage, _wolf_iwcwizardcallback_addwizardpage, cluadmex/IWCWizardCallback::AddWizardPage, mscs.iwcwizardcallback_addwizardpage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cluadmex.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - cluadmex.h
api_name:
 - IWCWizardCallback.AddWizardPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




## -remarks




<a href="https://msdn.microsoft.com/en-us/library/Aa369060(v=VS.85).aspx">Failover Cluster Administrator</a> extensions call the 
     <b>AddWizardPage</b> method from their 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370738(v=VS.85).aspx">IWEExtendWizard::CreateWizardPages</a> 
     methods. Before calling <b>AddWizardPage</b>, 
     extensions must call the function 
     <a href="https://msdn.microsoft.com/en-us/library/Bb760807(v=VS.85).aspx">CreatePropertySheetPage</a> to retrieve a 
     handle to pass in the <i>hpage</i> parameter.

Use 
     <a href="https://msdn.microsoft.com/en-us/library/Aa370512(v=VS.85).aspx">IWCWizard97Calllback::AddWizard97Page</a> 
     to add Wizard97 pages.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370512(v=VS.85).aspx">IWCWizard97Callback::AddWizard97Page</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370517(v=VS.85).aspx">IWCWizardCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa370738(v=VS.85).aspx">IWEExtendWizard::CreateWizardPages</a>
 

 

