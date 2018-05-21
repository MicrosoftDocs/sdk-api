---
UID: NC:netsh.NS_OSVERSIONCHECK
title: NS_OSVERSIONCHECK
author: windows-driver-content
description: Is the operating system check function for helpers.
old-location: netshell\ns_osversioncheck.htm
old-project: NetShell
ms.assetid: d58258ac-a16a-4983-bf35-71153dcbe652
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: NS_OSVERSIONCHECK, NS_OSVERSIONCHECK callback, NS_OSVERSIONCHECK callback function [NetShell], SampleOsVersionCheck, _netsh_ns_osversioncheck, netsh/NS_OSVERSIONCHECK, netshell.ns_osversioncheck
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NLM_USAGE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Netsh.h
api_name:
-	NS_OSVERSIONCHECK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NS_OSVERSIONCHECK callback function


## -description


The 
<b>NS_OSVERSIONCHECK</b> command is the operating system check function for helpers. This function can be called on a per-function basis, and verifies whether the associated function is supported on the specified operating system. This function is registered within the 
<a href="https://msdn.microsoft.com/dc0d6449-f635-417c-8363-51e61c417051">CMD_GROUP_ENTRY</a> or 
<a href="https://msdn.microsoft.com/299962c8-8f93-4b22-a232-8230eb64cc12">CMD_ENTRY</a> parameter of the 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The following is an example of an operating system check function. Be aware that <b>SampleOsVersionCheck</b> is a placeholder for the application-defined function name.


## -parameters




### -param CIMOSType [in]


### -param CIMOSProductSuite [in]


### -param CIMOSVersion [in]


### -param CIMOSBuildNumber [in]


### -param CIMServicePackMajorVersion [in]


### -param CIMServicePackMinorVersion [in]


### -param uiReserved


### -param dwReserved [in]


#### - CIMProcessorArchitecture [in]


## -returns



Returns <b>TRUE</b> of the command or group should be available, <b>FALSE</b> if the command or group should be hidden.




## -remarks



Parameters passed by this function are retrieved from WMI. Refer to the latest 
<a href="https://msdn.microsoft.com/ebc2e4aa-a77d-44a3-b649-3b3748bb267e">WMI documentation</a> to obtain these parameter definitions.

The operating system check function is useful for commands used by administrators who manage down-level servers or computers from a more recent version of Windows.




## -see-also




<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>



<a href="https://msdn.microsoft.com/4804152f-2042-4c6a-83c6-75c5e1ab7a04">Windows WMI</a>
 

 

