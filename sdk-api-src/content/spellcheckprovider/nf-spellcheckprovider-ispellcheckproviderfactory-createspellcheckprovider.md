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

# ISpellCheckProviderFactory::CreateSpellCheckProvider


## -description


Creates a spell checker (implemented by a spell check provider) that supports the specified language. This interface is not used directly by clients, but by the Spell Checking API.


## -parameters




### -param languageTag [in]

A <a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47</a> language tag that identifies the language for the requested spell checker.


### -param value [out, retval]

The created spell checker.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>languageTag</i> is an empty string, or there is no spell checker available for <i>languageTag</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>languageTag</i> is a null pointer.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/88689384-E95E-4D56-BAD4-9889816F76EB">ISpellCheckProviderFactory::IsSupported</a> can be called to determine if <i>languageTag</i> is supported.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=227302">BCP47 Tags for Identifying Languages</a>



<a href="https://msdn.microsoft.com/D7C8831E-6FCE-45E0-B2EB-4EB2B1F7911F">ISpellCheckProvider</a>



<a href="https://msdn.microsoft.com/680EC2D1-740E-40A8-9721-AC53AF17AC09">ISpellCheckProviderFactory</a>



<a href="https://msdn.microsoft.com/88689384-E95E-4D56-BAD4-9889816F76EB">ISpellCheckProviderFactory::IsSupported</a>
 

 

