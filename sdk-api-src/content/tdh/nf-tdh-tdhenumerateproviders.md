---
UID: NF:tdh.TdhEnumerateProviders
title: TdhEnumerateProviders function
author: windows-sdk-content
description: Retrieves a list of providers that have registered a MOF class or manifest file on the computer.
old-location: etw\tdhenumerateproviders_func.htm
old-project: etw
ms.assetid: ef326ef8-227d-46b5-88b9-b519748fb778
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: TdhEnumerateProviders, TdhEnumerateProviders function [ETW], etw.tdhenumerateproviders_func, tdh.tdhenumerateproviders_func, tdh/TdhEnumerateProviders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tdh.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TEMPLATE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - API-MS-Win-Eventing-Tdh-L1-1-0.dll
 - MinTdh.dll
api_name:
 - TdhEnumerateProviders
product: Windows
targetos: Windows
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TdhEnumerateProviders function


## -description


Retrieves a list of providers that have registered a MOF class or manifest file on the computer.


## -parameters




### -param pBuffer [out]

Array of providers that publicly define  their events on the computer. For details, see the <a href="https://msdn.microsoft.com/bb4548fb-70e5-4726-bc92-adb7ba7be0e4">PROVIDER_ENUMERATION_INFO</a> structure.


### -param pBufferSize [in, out]

Size, in bytes, of the <i>pBuffer</i> buffer. If the function succeeds, this parameter receives the size of the buffer used. If the buffer is too small, the function returns ERROR_INSUFFICIENT_BUFFER and sets this parameter to the required buffer size. If the buffer size is zero on input, no data is returned in the buffer and this parameter receives the required buffer size.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the <i>pBuffer</i> buffer is too small. Use the required buffer size set in <i>pBufferSize</i> to allocate a new buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
</table>
 




## -remarks



Because the number of registered event providers may fluctuate between calls to  this function, you should place this function in a loop that loops until the returned value is no longer ERROR_INSUFFICIENT_BUFFER.


#### Examples

For an example that shows how to enumerate providers, see <a href="https://msdn.microsoft.com/79a29a55-e211-4921-ac78-a21ef8ef238f">Enumerating Providers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ab34a433-b641-4408-81d5-c93609204d24">TdhEnumerateProviderFieldInformation</a>
 

 

