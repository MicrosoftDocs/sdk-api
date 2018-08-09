---
UID: NS:ipsectypes.IPSEC_KEYMODULE_STATE0_
title: IPSEC_KEYMODULE_STATE0_
author: windows-sdk-content
description: Stores Internet Protocol Security (IPsec) keying module specific information.
old-location: fwp\ipsec_keymodule_state0_struct.htm
old-project: fwp
ms.assetid: 5df02d3b-c61a-4c4b-a9ef-182c97a35f41
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPSEC_KEYMODULE_STATE0, IPSEC_KEYMODULE_STATE0 structure [Filtering], IPSEC_KEYMODULE_STATE0_, fwp.ipsec_keymodule_state0_struct, ipsectypes/IPSEC_KEYMODULE_STATE0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IPSEC_KEYMODULE_STATE0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_KEYMODULE_STATE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_KEYMODULE_STATE0_ structure


## -description


The <b>IPSEC_KEYMODULE_STATE0</b> structure stores Internet Protocol Security (IPsec) keying module specific information.


## -struct-fields




### -field keyModuleKey

The identifier of the keying module.


### -field stateBlob

A byte blob containing opaque keying module specific information.


## -remarks



<b>IPSEC_KEYMODULE_STATE0</b> is a specific implementation of IPSEC_KEYMODULE_STATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

