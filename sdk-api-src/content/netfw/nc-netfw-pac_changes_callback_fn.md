---
UID: NC:netfw.PAC_CHANGES_CALLBACK_FN
title: PAC_CHANGES_CALLBACK_FN (netfw.h)
description: Used to add custom behavior to the app container change notification process.
old-location: ics\pac_changes_callback_fn.htm
tech.root: ics
ms.assetid: 7a2afc36-c250-4eb1-9853-d79def85bb67
ms.date: 12/05/2018
ms.keywords: PAC_CHANGES_CALLBACK_FN, PAC_CHANGES_CALLBACK_FN callback, PAC_CHANGES_CALLBACK_FN callback function [ICS/ICF], ics.pac_changes_callback_fn, networkisolation/PAC_CHANGES_CALLBACK_FN
f1_keywords:
- netfw/PAC_CHANGES_CALLBACK_FN
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- networkisolation.h
api_name:
- PAC_CHANGES_CALLBACK_FN
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PAC_CHANGES_CALLBACK_FN callback function


## -description


The <b>PAC_CHANGES_CALLBACK_FN</b>  function is used to add custom behavior to the app container change notification process.


## -parameters




### -param *context [in, optional]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges">NetworkIsolationRegisterForAppContainerChanges</a> function.


### -param *pChange [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_change">INET_FIREWALL_AC_CHANGE</a>*</b>

The app container change information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges">NetworkIsolationRegisterForAppContainerChanges</a> to register this callback function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netfw/ns-netfw-inet_firewall_ac_change">INET_FIREWALL_AC_CHANGE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges">NetworkIsolationRegisterForAppContainerChanges</a>
 

 

