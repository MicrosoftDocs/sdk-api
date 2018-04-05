---
UID: NS:lpmapi.Error_Spec_IPv4
title: Error_Spec_IPv4
author: windows-driver-content
description: The Error_Spec_IPv4 structure stores error code information for RSVP transmissions.
old-location: qos\error_spec_ipv4.htm
old-project: QOS
ms.assetid: 23df7278-8f37-426f-98ff-0cf02d780b76
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: Error_Spec_IPv4, Error_Spec_IPv4 structure [QOS], lpmapi/Error_Spec_IPv4, qos.error_spec_ipv4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: Error_Spec_IPv4
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lpmapi.h
api_name:
-	Error_Spec_IPv4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Error_Spec_IPv4 structure


## -description


The 
<b>Error_Spec_IPv4</b> structure stores error code information for RSVP transmissions.


## -struct-fields




### -field errs_errnode

IP address of the node responsible for the error, in the form of an <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structure.


### -field errs_flags

Error flags. Must be one of the following:

<ul>
<li>ERROR_SPECF_InPlace</li>
<li>ERROR_SPECF_NotGuilty</li>
</ul>

### -field errs_code

Error code. Must be one of the following:

<ul>
<li>ERR_FORWARD_OK</li>
<li>ERR_Usage_globl</li>
<li>ERR_Usage_local</li>
<li>ERR_Usage_serv</li>
<li>ERR_global_mask</li>
</ul>

### -field errs_value

Error value.


## -see-also




<a href="https://msdn.microsoft.com/4d20cbb8-c29a-4c0c-bf06-532144da3e33">ERROR_SPEC</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a>
 

 

