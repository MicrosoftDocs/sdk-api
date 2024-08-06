---
UID: NC:netsh.NS_DLL_INIT_FN
title: NS_DLL_INIT_FN (netsh.h)
description: Called by NetShell to perform an initial loading of a helper.
helpviewer_keywords: ["InitHelperDll","NS_DLL_INIT_FN","NS_DLL_INIT_FN callback","NS_DLL_INIT_FN callback function [NetShell]","_netsh_inithelperdll","netsh/NS_DLL_INIT_FN","netshell.inithelperdll"]
old-location: netshell\inithelperdll.htm
tech.root: netshell
ms.assetid: 9af7e818-bb08-4d35-bab4-43cb94845f25
ms.date: 12/05/2018
ms.keywords: InitHelperDll, NS_DLL_INIT_FN, NS_DLL_INIT_FN callback, NS_DLL_INIT_FN callback function [NetShell], _netsh_inithelperdll, netsh/NS_DLL_INIT_FN, netshell.inithelperdll
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
 - NS_DLL_INIT_FN
 - netsh/NS_DLL_INIT_FN
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
 - NS_DLL_INIT_FN
---

# NS_DLL_INIT_FN callback function


## -description

The 
<b>InitHelperDll</b> function is called by NetShell to perform an initial loading of a helper.

## -parameters

### -param dwNetshVersion [in]

The version of NetShell.

### -param pReserved

Reserved for future use.

## -returns

Returns NO_ERROR upon success. Any other return value indicates an error.

## -remarks

The 
<b>InitHelperDll</b> function is the only function NetShell helpers are required to export. Helpers typically call the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registerhelper">RegisterHelper</a> function from within the 
<b>InitHelperDll</b> function, as shown in the following example:


``` syntax
DWORD
WINAPI
InitHelperDll(
    DWORD      dwNetshVersion,
    PVOID      pReserved
)
{
    NS_HELPER_ATTRIBUTES attMyAttributes;

    attMyAttributes.guidHelper = g_MyGuid;
    attMyAttributes.dwVersion  = 1;
    attMyAttributes.pfnStart   = NetshStartHelper;
    RegisterHelper( NULL, &attMyAttributes );

    return NO_ERROR;
}
```


## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registerhelper">RegisterHelper</a>
