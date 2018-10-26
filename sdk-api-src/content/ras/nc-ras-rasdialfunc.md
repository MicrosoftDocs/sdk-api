---
UID: NC:ras.RASDIALFUNC
title: RASDIALFUNC
author: windows-sdk-content
description: The RasDialFunc callback function is called by the RasDial function when a change of state occurs during a RAS connection process.
old-location: rras\rasdialfunc.htm
tech.root: rras
ms.assetid: 668ebede-73ec-4ee9-9b81-7167e827db60
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: RasDialFunc, RasDialFunc callback, RasDialFunc callback function [RAS], _ras_rasdialfunc, ras/RasDialFunc, rras.rasdialfunc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ras.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ras.h
api_name:
 - RasDialFunc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RASDIALFUNC callback function


## -description


The 
<b>RasDialFunc</b> callback function is called by the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function  when a change of state occurs during a RAS connection process.


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3








#### - dwError [in]

Specifies the error that has occurred, or zero if no error has occurred. 





<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> calls 
<b>RasDialFunc</b> with <i>dwError</i> set to zero upon entry to each connection state. If an error occurs within a state, 
<b>RasDialFunc</b> is called again with a nonzero <i>dwError</i> value.


#### - rasconnstate [in]

Specifies the 
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a> enumerator value that indicates the state the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> remote access connection process is about to enter.


#### - unMsg [in]

Specifies the type of event that has occurred. Currently, the only event defined is WM_RASDIALEVENT.


## -returns



This callback function does not return a value.




## -remarks



A 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> connection operation is suspended during a call to a 
<b>RasDialFunc</b> callback function. For that reason, the 
<b>RasDialFunc</b> implementation should generally return as quickly as possible. There are two exceptions to that rule. Asynchronous (slow) devices such as modems often have time-out periods measured in seconds rather than milliseconds; a slow return from a 
<b>RasDialFunc</b> function is generally not a problem. The prompt return requirement also does not apply when <i>dwError</i> is nonzero, indicating that an error has occurred. It is safe, for example, to put up an error dialog box and wait for user input.

The 
<b>RasDialFunc</b> implementation should not depend on the order or occurrence of particular 
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a> connection states, because this may vary between platforms.

Do not call the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function from within a 
<b>RasDialFunc</b> callback function. Call the 
<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>, 
<a href="https://msdn.microsoft.com/9df7402f-c93e-45d4-925a-f2ce9d547bce">RasEnumEntries</a>, 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>, 
<a href="https://msdn.microsoft.com/4d308dd8-e623-467b-836e-faace19460f1">RasGetErrorString</a>, and 
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a> functions from within the callback function. For example, calling 
<b>RasGetConnectStatus</b> from within a callback function would be useful to  determine the name and type of the connecting device.

<div class="alert"><b>Note</b>  For convenience, 
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a> can be called from within a 
<b>RasDialFunc</b> callback function. However, much of the hang-up processing occurs after the 
<b>RasDialFunc</b> callback function has returned.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>RasDialFunc</b> is a placeholder for the application-defined or library-defined function name.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCONNSTATE</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/f0b0dbbc-8544-4711-819a-48bb714a67d9">RasDialFunc1</a>



<a href="https://msdn.microsoft.com/a9395048-492b-42fb-b247-52999cee3f44">RasDialFunc2</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/9df7402f-c93e-45d4-925a-f2ce9d547bce">RasEnumEntries</a>



<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>



<a href="https://msdn.microsoft.com/4d308dd8-e623-467b-836e-faace19460f1">RasGetErrorString</a>



<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

