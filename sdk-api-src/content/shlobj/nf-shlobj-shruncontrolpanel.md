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

# SHRunControlPanel function


## -description


Opens a Control Panel item.
            
<div class="alert"><b>Note</b>  This function is not supported as of Windows Vista</div><div> </div>

## -parameters




### -param lpcszCmdLine [in]

Type: <b>PCWSTR</b>

Pointer to a string that contains the command line that opens the Control Panel item. This command line includes at least the name of the .cpl file. It can also contain any other necessary information such as the property sheet page within the item (either by ordinal or by name). For more information, see <a href="https://msdn.microsoft.com/c17167ab-e9a0-4290-955c-484d038b82af">Executing Control Panel Items</a>.


### -param hwndMsgParent [in, optional]

Type: <b>HWND</b>

The handle of the parent window, used to display error messages about the opening of the item. This value can be <b>NULL</b>.


## -returns



Type: <b>BOOL</b>

<b>TRUE</b> if the Control Panel item was opened successfully; otherwise, <b>FALSE</b>. 

                    

As of Windows Vista, this function always returns <b>FALSE</b>.




## -remarks



If the specified Control Panel item is already running, <b>SHRunControlPanel</b> attempts to switch to that instance rather than opening a new instance.


#### Examples

Example calls to <b>SHRunControlPanel</b> are shown here.

<pre class="syntax" xml:space="preserve"><code>SHRunControlPanel(TEXT("timedate.cpl"), hwnd);
SHRunControlPanel(L"appwiz.cpl", NULL);
SHRunControlPanel(L"appwiz.cpl,2", NULL);
SHRunControlPanel("desk.cpl,Settings", hwnd</code></pre>


