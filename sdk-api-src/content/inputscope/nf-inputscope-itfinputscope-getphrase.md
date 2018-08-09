---
UID: NF:inputscope.ITfInputScope.GetPhrase
title: ITfInputScope::GetPhrase
author: windows-sdk-content
description: ITfInputScope::GetPhrase method
old-location: tsf\itfinputscope_getphrase.htm
old-project: TSF
ms.assetid: 9a97dab0-2e3d-4921-80a6-0f2c79fbf4aa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPhrase, GetPhrase method [Text Services Framework], GetPhrase method [Text Services Framework],ITfInputScope interface, ITfInputScope interface [Text Services Framework],GetPhrase method, ITfInputScope.GetPhrase, ITfInputScope::GetPhrase, inputscope/ITfInputScope::GetPhrase, tsf.itfinputscope_getphrase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InputScope
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputScope.GetPhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputScope::GetPhrase


## -description




## -parameters




### -param ppbstrPhrases [out]

Pointer to an array of pointers to strings containing phrases. The calling function must call <b>SystFreeString()</b> to free the memory allocated to the strings and <b>CoTaskMemFree</b> to free the buffer.


### -param pcCount [out]

Pointer to the number of phrases returned.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 



