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
 

 

