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

# NS_HELPER_START_FN callback function


## -description


The 
<b>NS_HELPER_START_FN</b> command is the start function for helpers. The start function provides an opportunity for helpers to register contexts and is registered in the 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The following is an example of a start function. Be aware that <b>SampleStartHelper</b> is a placeholder for the application-defined function name.


## -parameters




### -param *pguidParent [in]

The parent under which the helper DLL should be registered.


### -param dwVersion [in]

The version of the parent helper DLL.


## -returns



Returns NO_ERROR upon success. Any other return value indicates an error.




## -remarks



A typical implementation of the start function is as follows:

<pre class="syntax" xml:space="preserve"><code>DWORD WINAPI SampleStartHelper(
    CONST GUID *pguidParent,
    DWORD       dwVersion
)
{
    DWORD dwErr;
    NS_CONTEXT_ATTRIBUTES attMyAttributes;

    ZeroMemory(&amp;attMyAttributes, sizeof(attMyAttributes));
    attMyAttributes.pwszContext   = L"samplecontext";
    attMyAttributes.guidHelper    = g_SampleGuid;
    attMyAttributes.dwVersion     = 1;
    attMyAttributes.dwFlags       = 0;
    attMyAttributes.ulNumTopCmds  = g_ulSampleNumTopCmds;
    attMyAttributes.pTopCmds      = (CMD_ENTRY (*)[])&amp;g_SampleTopCmds;
    attMyAttributes.ulNumGroups   = g_ulSampleCmdGroups; 
    attMyAttributes.pCmdGroups    = (CMD_GROUP_ENTRY (*)[])&amp;g_SampleCmdsGroups;
    attMyAttributes.pfnCommitFn   = SampleCommit;
    attMyAttributes.pfnDumpFn     = SampleDump;
    attMyAttributes.pfnConnectFn  = SampleConnect;

    dwErr = RegisterContext( &amp;attMyAttributes );
    return dwErr;
}</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/a56c11e6-5314-43eb-9960-55987395112f">NS_HELPER_STOP_FN</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 

