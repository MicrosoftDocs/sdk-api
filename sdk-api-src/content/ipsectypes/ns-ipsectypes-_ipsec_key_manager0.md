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

# _IPSEC_KEY_MANAGER0 structure


## -description


The <b>IPSEC_KEY_MANAGER0</b> structure is  used to register key management callbacks with IPsec.


## -struct-fields




### -field keyManagerKey

Type: <b>GUID</b>

Uniquely identifies the Key Manager.


### -field displayData

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a></b>

Contains annotations associated with the filter.


### -field flags

Type: <b>UINT32</b>

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY"></a><a id="ipsec_key_manager_flag_dictate_key"></a><dl>
<dt><b>IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
Specifies that the TIA will be able to accept key notifications and also potentially dictate keys. If this flag is not set, the TIA can only accept key notifications and will not be able to dictate keys.

</td>
</tr>
</table>
 


### -field keyDictationTimeoutHint

Type: <b>UINT8</b>

Time, in seconds, after which the <b>keyDictation</b> callback must return in order for registration to succeed. Set this field to <b>0</b> in order to use the default timeout (5 seconds). 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/736ea54d-ca17-4cb5-bcb2-95b4377f321c">IPSEC_KEY_MANAGER_CALLBACKS0</a>



<a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

