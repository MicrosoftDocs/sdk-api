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

# _CMD_ENTRY structure


## -description


The 
<b>CMD_ENTRY</b> structure defines a helper command.


## -struct-fields




### -field pwszCmdToken

The token (name) for the command.


### -field pfnCmdHandler

A function that handles the command. For more information, see 
<a href="https://msdn.microsoft.com/5058e202-9ad4-4789-97db-3c13b4a1c337">FN_HANDLE_CMD</a>.


### -field dwShortCmdHelpToken

A short help message. This is the message identifier from the resource file of the helper DLL.


### -field dwCmdHlpToken

The message to display if the command is followed only by a help token (HELP, /?, -?, or ?). This is the message identifier from the resource file of the helper DLL.


### -field dwFlags

The flags for the command. For more information, see 
<a href="https://msdn.microsoft.com/61dfa4ae-cf70-4858-be10-f77a318eaa28">Netshell Flags</a>.


### -field pOsVersionCheck

The operating system version check function. This is the function used to determine whether the command can be run on the operating system running on the local and/or remote context before invoking or displaying commands. For more information, see 
<a href="https://msdn.microsoft.com/d58258ac-a16a-4983-bf35-71153dcbe652">NS_OSVERSIONCHECK</a>.


## -remarks



Macros are available that can simplify the creation of the 
<b>CMD_ENTRY</b> structure, as follows:

<pre class="syntax" xml:space="preserve"><code>#define CREATE_CMD_ENTRY_EX(t,f,i)       {CMD_##t, f, HLP_##t, HLP_##t##_EX, i, NULL}
#define CREATE_CMD_ENTRY_EX_VER(t,f,i,v) {CMD_##t, f, HLP_##t, HLP_##t##_EX, i, v}
#define CREATE_CMD_ENTRY(t,f)            {CMD_##t, f, HLP_##t, HLP_##t##_EX, CMD_FLAG_PRIVATE, NULL}</code></pre>
If these macros are used, the following constants must be defined in the helper DLL:



The following are example uses of these macros:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define HLP_SAMPLE_ADD_BAR        1001
#define HLP_SAMPLE_ADD_BAR_EX     1002
#define HLP_SAMPLE_DELETE_BAR     1003
#define HLP_SAMPLE_DELETE_BAR_EX  1004
#define HLP_SAMPLE_SET_GLOBAL     1005
#define HLP_SAMPLE_SET_GLOBAL_EX  1006
#define HLP_SAMPLE_SET_BAR        1007
#define HLP_SAMPLE_SET_BAR_EX     1008
#define HLP_SAMPLE_SET_FILTER     1009
#define HLP_SAMPLE_SET_FILTER_EX  1010
#define HLP_SAMPLE_SHOW_GLOBAL    1011
#define HLP_SAMPLE_SHOW_GLOBAL_EX 1012
#define HLP_SAMPLE_SHOW_BAR       1013
#define HLP_SAMPLE_SHOW_BAR_EX    1014
#define HLP_SAMPLE_SHOW_FILTER    1015
#define HLP_SAMPLE_SHOW_FILTER_EX 1016

#define CMD_SAMPLE_ADD_BAR        L"add_bar"
#define CMD_SAMPLE_DELETE_BAR     L"delete_bar"
#define CMD_SAMPLE_SET_GLOBAL     L"set_global"
#define CMD_SAMPLE_SET_BAR        L"set_bar"
#define CMD_SAMPLE_SET_FILTER     L"set_filter"
#define CMD_SAMPLE_SHOW_GLOBAL    L"show_global"
#define CMD_SAMPLE_SHOW_BAR       L"show_bar"
#define CMD_SAMPLE_SHOW_FILTER    L"show_filter"

CMD_ENTRY  g_SampleAddCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_ADD_BAR, HandleSampleAddBar),
};
CMD_ENTRY  g_SampleDeleteCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_DELETE_BAR, HandleSampleDeleteBar),
};
CMD_ENTRY  g_SampleSetCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_SET_GLOBAL, HandleSampleSetGlobal),
    CREATE_CMD_ENTRY_EX(SAMPLE_SET_BAR, HandleSampleSetBar, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE) ),
    CREATE_CMD_ENTRY_EX_VER(SAMPLE_SET_FILTER, HandleSampleSetFilter, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE), CheckRunningOnWindowsXP),
};
CMD_ENTRY  g_SampleShowCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_SHOW_GLOBAL, HandleSampleShowGlobal),
    CREATE_CMD_ENTRY_EX(SAMPLE_SHOW_BAR, HandleSampleShowBar, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE) ),
    CREATE_CMD_ENTRY_EX_VER(SAMPLE_SHOW_FILTER, HandleSampleShowFilter, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE), CheckRunningOnWindowsXP),
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dc0d6449-f635-417c-8363-51e61c417051">CMD_GROUP_ENTRY</a>



<a href="https://msdn.microsoft.com/2380cd4e-5e41-4bfb-874c-50be09044c85">NS_CONTEXT_COMMIT_FN</a>



<a href="https://msdn.microsoft.com/61dfa4ae-cf70-4858-be10-f77a318eaa28">NetShell Flags</a>
 

 

