---
UID: NC:netfw.PAC_CHANGES_CALLBACK_FN
title: PAC_CHANGES_CALLBACK_FN
author: windows-sdk-content
description: Used to add custom behavior to the app container change notification process.
old-location: ics\pac_changes_callback_fn.htm
old-project: ICS
ms.assetid: 7a2afc36-c250-4eb1-9853-d79def85bb67
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: PAC_CHANGES_CALLBACK_FN, PAC_CHANGES_CALLBACK_FN callback, PAC_CHANGES_CALLBACK_FN callback function [ICS/ICF], ics.pac_changes_callback_fn, networkisolation/PAC_CHANGES_CALLBACK_FN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: netfw.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NETCON_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	networkisolation.h
api_name:
-	PAC_CHANGES_CALLBACK_FN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PAC_CHANGES_CALLBACK_FN callback function


## -description


The <b>PAC_CHANGES_CALLBACK_FN</b>  function is used to add custom behavior to the app container change notification process.


## -parameters




### -param *context [in, optional]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a> function.


### -param *pChange [in]

Type: <b>const <a href="https://msdn.microsoft.com/b5f1b85d-3538-4be3-b97b-f9207cc7063b">INET_FIREWALL_AC_CHANGE</a>*</b>

The app container change information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a> to register this callback function.




## -see-also




<a href="https://msdn.microsoft.com/b5f1b85d-3538-4be3-b97b-f9207cc7063b">INET_FIREWALL_AC_CHANGE</a>



<a href="https://msdn.microsoft.com/2affb2a8-224c-4d2d-86e2-f194d3990dbe">NetworkIsolationRegisterForAppContainerChanges</a>
 

 

