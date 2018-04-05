---
UID: NF:comadmin.ICOMAdminCatalog.InstallMultipleEventClasses
title: ICOMAdminCatalog::InstallMultipleEventClasses method
author: windows-driver-content
description: Installs event classes from multiple files into a COM+ application.
old-location: cos\icomadmincatalog_installmultipleeventclasses.htm
old-project: cossdk
ms.assetid: 12860254-4658-4e0d-ad00-7e25875037bf
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ICOMAdminCatalog, ICOMAdminCatalog interface [COM+], InstallMultipleEventClasses method, ICOMAdminCatalog::InstallMultipleEventClasses, InstallMultipleEventClasses method [COM+], InstallMultipleEventClasses method [COM+], ICOMAdminCatalog interface, InstallMultipleEventClasses,ICOMAdminCatalog.InstallMultipleEventClasses, _cos_ICOMAdminCatalog_InstallMultipleEventClasses, comadmin/ICOMAdminCatalog::InstallMultipleEventClasses, cos.icomadmincatalog_installmultipleeventclasses
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog.InstallMultipleEventClasses
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog::InstallMultipleEventClasses method


## -description


Installs event classes from multiple files into a COM+ application.


## -parameters




### -param bstrApplIdOrName [in]

The GUID or name of the application.


### -param ppsaVarFileNames [in]

An array of the names of the DLL files that contains the event classes to be installed.


### -param ppsaVarCLSIDS [in]

An array of CLSIDs for the event classes to be installed.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Use <b>InstallMultipleEventClasses</b> to install event classes from DLLs holding dummy implementations of the event classes. The requirements are a self-registering DLL, a type library describing the interfaces implemented by the event classes, and each event class having a CLSID and a ProgID. 



The dummy implementation of the interface exposed by an event class never actually runs; it exists only to register the event class. Instead, when the event class is created by the publisher, an implementation is provided by the Events system to send the event to subscribers. 






## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

