---
UID: NF:wbemdisp.ISWbemObjectEx.Refresh_
title: ISWbemObjectEx::Refresh_
author: windows-sdk-content
description: Updates the data for objects that have data supplied by a performance provider, such as the Performance Counter Classes. You can obtain updated data more quickly and without a call to SWbemServices.Get_.
old-location: wmi\swbemobjectex_refresh_.htm
old-project: WmiSdk
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemObjectEx interface [Windows Management Instrumentation],Refresh_ method, ISWbemObjectEx.Refresh_, ISWbemObjectEx::Refresh_, Refresh_, Refresh_ method [Windows Management Instrumentation], Refresh_ method [Windows Management Instrumentation],ISWbemObjectEx interface, Refresh_ method [Windows Management Instrumentation],SWbemObjectEx object, SWbemObjectEx object [Windows Management Instrumentation],Refresh_ method, SWbemObjectEx.Refresh_, _hmm_swbemobjectex.refresh_, wmi.swbemobjectex_refresh_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemObjectEx.Refresh_
 - ISWbemObjectEx.Refresh_
 - ISWbemObjectEx.Refresh_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectEx::Refresh_


## -description


The 
<b>Refresh_</b> method of <a href="https://msdn.microsoft.com/944d4cdc-ad35-4b53-b755-f10131a087fb">SWbemObjectEx</a> updates the data for objects that have data supplied by a performance provider, such as the <a href="https://msdn.microsoft.com/71746363-6fec-4344-8c5e-5cc057ebdf76">Performance Counter Classes</a>. You can obtain updated data more quickly and without a call to <a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get_</a>.

For more information about this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

Reserved operation flags which, if specified, must be 0 (zero).


### -param objWbemNamedValueSet [in, optional]

An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that sets context for the operation.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d">Monitoring Performance Data</a>



<a href="https://msdn.microsoft.com/944d4cdc-ad35-4b53-b755-f10131a087fb">SWbemObjectEx</a>
 

 

