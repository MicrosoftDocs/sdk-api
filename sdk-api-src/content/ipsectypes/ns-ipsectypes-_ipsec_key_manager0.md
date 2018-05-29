---
UID: NS:ipsectypes._IPSEC_KEY_MANAGER0
title: "_IPSEC_KEY_MANAGER0"
author: windows-sdk-content
description: Used to register key management callbacks with IPsec.
old-location: fwp\ipsec_key_manager0.htm
old-project: FWP
ms.assetid: 942F38AF-13F4-4A2E-A504-5085EC90E74C
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_KEY_MANAGER0, IPSEC_KEY_MANAGER0 structure [Filtering], IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY, _IPSEC_KEY_MANAGER0, fwp.ipsec_key_manager0, ipsectypes/IPSEC_KEY_MANAGER0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IPSEC_KEY_MANAGER0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ipsectypes.h
api_name:
-	IPSEC_KEY_MANAGER0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

