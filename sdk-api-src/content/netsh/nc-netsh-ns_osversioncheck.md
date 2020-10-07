---
UID: NC:netsh.NS_OSVERSIONCHECK
title: NS_OSVERSIONCHECK (netsh.h)
description: Is the operating system check function for helpers.
helpviewer_keywords: ["NS_OSVERSIONCHECK","NS_OSVERSIONCHECK callback","NS_OSVERSIONCHECK callback function [NetShell]","SampleOsVersionCheck","_netsh_ns_osversioncheck","netsh/NS_OSVERSIONCHECK","netshell.ns_osversioncheck"]
old-location: netshell\ns_osversioncheck.htm
tech.root: netshell
ms.assetid: d58258ac-a16a-4983-bf35-71153dcbe652
ms.date: 12/05/2018
ms.keywords: NS_OSVERSIONCHECK, NS_OSVERSIONCHECK callback, NS_OSVERSIONCHECK callback function [NetShell], SampleOsVersionCheck, _netsh_ns_osversioncheck, netsh/NS_OSVERSIONCHECK, netshell.ns_osversioncheck
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NS_OSVERSIONCHECK
 - netsh/NS_OSVERSIONCHECK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Netsh.h
api_name:
 - NS_OSVERSIONCHECK
---

# NS_OSVERSIONCHECK callback function


## -description

The 
<b>NS_OSVERSIONCHECK</b> command is the operating system check function for helpers. This function can be called on a per-function basis, and verifies whether the associated function is supported on the specified operating system. This function is registered within the 
<a href="/windows/desktop/api/netsh/ns-netsh-cmd_group_entry">CMD_GROUP_ENTRY</a> or 
<a href="/windows/desktop/api/netsh/ns-netsh-cmd_entry">CMD_ENTRY</a> parameter of the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> function. The following is an example of an operating system check function. Be aware that <b>SampleOsVersionCheck</b> is a placeholder for the application-defined function name.

## -parameters

### -param CIMOSType [in]

### -param CIMOSProductSuite [in]

### -param CIMOSVersion [in]

### -param CIMOSBuildNumber [in]

### -param CIMServicePackMajorVersion [in]

### -param CIMServicePackMinorVersion [in]

### -param uiReserved

### -param dwReserved [in]


## -returns

Returns <b>TRUE</b> of the command or group should be available, <b>FALSE</b> if the command or group should be hidden.

## -remarks

Parameters passed by this function are retrieved from WMI. Refer to the latest 
<a href="/windows/desktop/WmiSdk/wmi-reference">WMI documentation</a> to obtain these parameter definitions.

The operating system check function is useful for commands used by administrators who manage down-level servers or computers from a more recent version of Windows.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>



<a href="/windows/desktop/WmiSdk/wmi-start-page">Windows WMI</a>