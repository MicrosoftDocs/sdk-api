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

# _IPSEC_KEY_MANAGER_CALLBACKS0 structure


## -description


The <b>IPSEC_KEY_MANAGER_CALLBACKS0</b> structure specifies the set of callbacks which should be invoked by IPsec at various stages of SA negotiation


## -struct-fields




### -field reserved

Type: <b>GUID</b>

Reserved for system use.


### -field flags

Type: <b>UINT32</b>

Reserved for system use.


### -field keyDictationCheck

Type: <b><a href="https://msdn.microsoft.com/0B91B57C-6943-4702-8926-8ED2B7B3E48D">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a></b>

Specifies that the Trusted Intermediary Agent (TIA) will dictate the keys for the SA being negotiated. Only used if the <b>IPSEC_DICTATE_KEY</b> flag is set.


### -field keyDictation

Type: <b><a href="https://msdn.microsoft.com/A69E44FF-A58D-426B-BD59-8EB4B5A63B66">IPSEC_KEY_MANAGER_DICTATE_KEY0</a></b>

Allows the TIA to dictate the keys for the SA being negotiated. Only used if the <b>IPSEC_DICTATE_KEY</b> flag is set.


### -field keyNotify

Type: <b><a href="https://msdn.microsoft.com/ECB904D1-C78F-493D-A6B8-73EA782EA935">IPSEC_KEY_MANAGER_NOTIFY_KEY0</a></b>

Notifies the TIA of the keys for the SA being negotiated.


## -remarks



If the <b>IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY</b> flag is set, all three callbacks must be specified; otherwise, only the <b>keyNotify</b> callback should be specified.




## -see-also




<a href="https://msdn.microsoft.com/942F38AF-13F4-4A2E-A504-5085EC90E74C">IPSEC_KEY_MANAGER0</a>



<a href="https://msdn.microsoft.com/A69E44FF-A58D-426B-BD59-8EB4B5A63B66">IPSEC_KEY_MANAGER_DICTATE_KEY0</a>



<a href="https://msdn.microsoft.com/0B91B57C-6943-4702-8926-8ED2B7B3E48D">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a>



<a href="https://msdn.microsoft.com/ECB904D1-C78F-493D-A6B8-73EA782EA935">IPSEC_KEY_MANAGER_NOTIFY_KEY0</a>



<a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

