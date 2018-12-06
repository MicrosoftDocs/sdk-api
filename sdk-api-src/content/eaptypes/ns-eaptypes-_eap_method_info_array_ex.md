---
UID: NS:eaptypes._EAP_METHOD_INFO_ARRAY_EX
title: "_EAP_METHOD_INFO_ARRAY_EX"
author: windows-sdk-content
description: Contains information about all of the EAP methods installed on the client computer.
old-location: eaphost\eap_method_info_array_ex.htm
tech.root: eaphost
ms.assetid: 3deb04da-3071-4ddd-a7cb-82a1c47c3677
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EAP_METHOD_INFO_ARRAY_EX, EAP_METHOD_INFO_ARRAY_EX structure [EAPHost], PEAP_METHOD_INFO_ARRAY_EX, PEAP_METHOD_INFO_ARRAY_EX structure pointer [EAPHost], _EAP_METHOD_INFO_ARRAY_EX, eaphost.eap_method_info_array_ex, eaptypes/EAP_METHOD_INFO_ARRAY_EX, eaptypes/PEAP_METHOD_INFO_ARRAY_EX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_METHOD_INFO_ARRAY_EX
product: Windows
targetos: Windows
req.typenames: EAP_METHOD_INFO_ARRAY_EX
req.redist: 
---

# _EAP_METHOD_INFO_ARRAY_EX structure


## -description


The <b>EAP_METHOD_INFO_ARRAY_EX</b> structure contains information about all of the EAP methods installed on the client computer. After populating <b>EAP_METHOD_INFO_ARRAY_EX</b>, EAPHost passes this method information to the supplicant.


## -struct-fields




### -field dwNumberOfMethods

The number of <a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a> structures in <b>pEapMethods</b>.


### -field pEapMethods

Pointer to the address of the first element in an array of <a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a> structures. The total number of elements is specified in <b>dwNumberOfMethods</b>.


## -see-also




<a href="https://msdn.microsoft.com/f6f3b909-1e89-47f8-853c-c0f3f2414817">Common EAPHost API Structures</a>



<a href="https://msdn.microsoft.com/10407b85-5d2c-4c75-9b65-a0d65d4cc7ab">EAP Method Properties</a>



<a href="https://msdn.microsoft.com/89b5dcbd-afa9-40a8-ab04-2caee01ce0a3">EAP_METHOD_INFO</a>



<a href="https://msdn.microsoft.com/a3e2d5c0-eacd-46de-b092-6fd749870881">EAP_METHOD_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/2d25f418-2130-4f9c-b3f4-f639dfba020a">EAP_METHOD_INFO_EX</a>



<a href="https://msdn.microsoft.com/47702dd9-d9c2-4dd5-a12d-23a55b031d27">EAP_METHOD_TYPE</a>
 

 

