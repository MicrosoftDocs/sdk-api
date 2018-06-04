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

# InitOnceInitialize function


## -description


Initializes a one-time initialization structure.


## -parameters




### -param InitOnce [out]

A pointer to the one-time initialization structure.


## -returns



This function does not return a value.




## -remarks



The <b>InitOnceInitialize</b> function is used to initialize a one-time initialization structure dynamically. To initialize the structure statically, assign the constant <b>INIT_ONCE_STATIC_INIT</b> to the structure variable.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.

A one-time initialization object cannot be moved or copied. The process must not modify the initialization object, and must instead treat it as logically opaque. Only use the one-time initialization functions to manage one-time initialization objects.


#### Examples

The following example calls <b>InitOnceInitialize</b> to initialize the one-time initialization structure named <code>InitOnce</code>. Alternatively, the structure can be declared as a global variable as shown in <a href="https://msdn.microsoft.com/47e68fbb-29f8-4930-beba-01d44263eb1e">Using One-Time Initialization</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
//Requires Windows Vista, Windows Server 2008 or later
#define _WIN32_WINNT 0x0600

#include &lt;windows.h&gt;

BOOL StartInitialization()
{
    INIT_ONCE InitOnce;

    InitOnceInitialize(&amp;InitOnce);

    //...
    return TRUE;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/04c161ed-d1b0-4995-b246-cb64cb67ae47">InitOnceExecuteOnce</a>



<a href="https://msdn.microsoft.com/404c083c-7bee-44c2-b8e7-da1901b6ab2f">One-Time Initialization</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

