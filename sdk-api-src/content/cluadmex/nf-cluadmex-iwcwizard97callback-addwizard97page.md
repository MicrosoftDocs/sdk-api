---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWCWizard97Callback::AddWizard97Page


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements 
    section. Support for this method was removed in Windows Server 2008.]

Adds a Wizard97 property page to a Wizard97 wizard, such as the Failover Cluster Application Wizard.


## -parameters




### -param hpage [in]

Handle to the property page to be added.


## -returns



If <b>AddWizard97Page</b> is not 
       successful, it can return other <b>HRESULT</b> values.




## -remarks




<a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Failover Cluster Administrator</a> extensions call the 
     <b>AddWizard97Page</b> method from their 
     <a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a> 
     methods. Before calling 
     <b>AddWizard97Page</b>, extensions must 
     call the function <a href="_win32_createpropertysheetpage_cpp">CreatePropertySheetPage</a> 
     to retrieve a handle to pass in the <i>hpage</i> parameter.

To add non-Wizard97 pages, use 
     <a href="https://msdn.microsoft.com/e5ce7798-c1e6-47b6-a1bf-1262b3511b22">IWCWizardCallback::AddWizardPage</a>.




## -see-also




<a href="https://msdn.microsoft.com/cbde3bcf-8242-49dc-9ac0-a4b078ea526e">IWCWizard97Callback</a>



<a href="https://msdn.microsoft.com/e5ce7798-c1e6-47b6-a1bf-1262b3511b22">IWCWizardCallback::AddWizardPage</a>



<a href="https://msdn.microsoft.com/1ab81008-42d8-4863-8836-0508e49ceca9">IWEExtendWizard97::CreateWizard97Pages</a>
 

 

