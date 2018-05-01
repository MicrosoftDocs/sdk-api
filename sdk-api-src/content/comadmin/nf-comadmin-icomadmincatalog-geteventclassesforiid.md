---
UID: NF:comadmin.ICOMAdminCatalog.GetEventClassesForIID
title: ICOMAdminCatalog::GetEventClassesForIID method
author: windows-driver-content
description: Retrieves a list of the event classes registered on the computer that implement a specified interface.
old-location: cos\icomadmincatalog_geteventclassesforiid.htm
old-project: cossdk
ms.assetid: 9f1a77ef-3dfd-4402-a05a-9cb4fd50dbd8
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: GetEventClassesForIID method [COM+], GetEventClassesForIID method [COM+], ICOMAdminCatalog interface, GetEventClassesForIID,ICOMAdminCatalog.GetEventClassesForIID, ICOMAdminCatalog, ICOMAdminCatalog interface [COM+], GetEventClassesForIID method, ICOMAdminCatalog::GetEventClassesForIID, _cos_ICOMAdminCatalog_GetEventClassesForIID, comadmin/ICOMAdminCatalog::GetEventClassesForIID, cos.icomadmincatalog_geteventclassesforiid
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
-	ICOMAdminCatalog.GetEventClassesForIID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog::GetEventClassesForIID method


## -description


Retrieves a list of the event classes registered on the computer that implement a specified interface.


## -parameters




### -param bstrIID [in]

A GUID representing the interface for which event classes should be found. If this parameter is <b>NULL</b>, the method retrieves all event classes registered on the computer.


### -param ppsaVarCLSIDs [out]

An array of CLSIDs for the event classes implementing the interface specified in <i>bstrIID</i>.


### -param ppsaVarProgIDs [out]

An array of ProgIDs for the event classes implementing the interface specified in <i>bstrIID</i>.


### -param ppsaVarDescriptions [out]

An array of descriptions for the event classes implementing the interface specified in <i>bstrIID</i>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a>
 

 

