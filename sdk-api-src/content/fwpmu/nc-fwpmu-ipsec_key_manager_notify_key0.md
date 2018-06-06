---
UID: NC:fwpmu.IPSEC_KEY_MANAGER_NOTIFY_KEY0
title: IPSEC_KEY_MANAGER_NOTIFY_KEY0
author: windows-sdk-content
description: Is used to notify Trusted Intermediary Agents (TIAs) of the keys for the SA being negotiated.
old-location: fwp\ipsec_key_manager_notify_key0.htm
old-project: FWP
ms.assetid: ECB904D1-C78F-493D-A6B8-73EA782EA935
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_KEY_MANAGER_NOTIFY_KEY0, IPSEC_KEY_MANAGER_NOTIFY_KEY0 function, IPSEC_KEY_MANAGER_NOTIFY_KEY0 function pointer [Filtering], fwp.ipsec_key_manager_notify_key0, fwp.ipsec_key_notify_key0, fwpmu/IPSEC_KEY_MANAGER_NOTIFY_KEY0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
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
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_NOTIFY_KEY0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IPSEC_KEY_MANAGER_NOTIFY_KEY0 callback function


## -description


The IPSEC_KEY_MANAGER_NOTIFY_KEY0 function is used to notify Trusted Intermediary Agents (TIAs) of the keys for the SA being negotiated.


## -parameters




### -param *inboundSa [in]

Type: <b>const <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a>*</b>

Information about the inbound SA.


### -param *outboundSa [in]

Type: <b>const <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a>*</b>

Information about the outbound SA.


## -returns



This function pointer does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister</a> to register this function pointer.




## -see-also




<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>



<a href="https://msdn.microsoft.com/e63db9e6-af26-4511-99fa-7d0b13d409d8">Windows Filtering Platform  API Reference</a>
 

 

