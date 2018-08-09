---
UID: NC:netsh.NS_DLL_INIT_FN
title: NS_DLL_INIT_FN
author: windows-sdk-content
description: Called by NetShell to perform an initial loading of a helper.
old-location: netshell\inithelperdll.htm
old-project: netshell
ms.assetid: 9af7e818-bb08-4d35-bab4-43cb94845f25
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitHelperDll, NS_DLL_INIT_FN, NS_DLL_INIT_FN callback, NS_DLL_INIT_FN callback function [NetShell], _netsh_inithelperdll, netsh/NS_DLL_INIT_FN, netshell.inithelperdll
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NLM_USAGE_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Netsh.h
api_name:
 - NS_DLL_INIT_FN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a> function from within the 
<b>InitHelperDll</b> function, as shown in the following example:

<pre class="syntax" xml:space="preserve"><code>DWORD
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
    RegisterHelper( NULL, &amp;attMyAttributes );

    return NO_ERROR;
}</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a>
 

 

