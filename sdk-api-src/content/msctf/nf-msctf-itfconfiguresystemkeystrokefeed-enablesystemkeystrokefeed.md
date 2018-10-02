---
UID: NF:msctf.ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed
title: ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed
author: windows-sdk-content
description: ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed method
old-location: tsf\itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed.htm
tech.root: TSF
ms.assetid: 66dc5db3-c4d9-422e-bbc0-300409a9576a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EnableSystemKeystrokeFeed, EnableSystemKeystrokeFeed method [Text Services Framework], EnableSystemKeystrokeFeed method [Text Services Framework],ITfConfigureSystemKeystrokeFeed interface, ITfConfigureSystemKeystrokeFeed interface [Text Services Framework],EnableSystemKeystrokeFeed method, ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed, ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed, _tsf_itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed_ref, msctf/ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed, tsf.itfconfiguresystemkeystrokefeed_enablesystemkeystrokefeed
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfConfigureSystemKeystrokeFeed.EnableSystemKeystrokeFeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed


## -description




## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There was no corresponding call to DisableSystemKeystrokeFeed.

</td>
</tr>
</table>
 




## -remarks



By default, the TSF manager will process keystrokes and pass them to the text services. An application prevents this by calling <b>DisableSystemKeystrokeFeed</b> .

Calls to <b>DisableSystemKeystrokeFeed</b> are cumulative, so every call to <b>DisableSystemKeystrokeFeed</b> requires a subsequent call to <b>EnableSystemKeystrokeFeed</b>. Calling <b>EnableSystemKeystrokeFeed</b> will not enable keystroke processing if <b>DisableSystemKeystrokeFeed</b> is called more than once.




## -see-also




<a href="https://msdn.microsoft.com/9b15d628-87aa-4e20-b9c3-fb29a79683cb">ITfConfigureSystemKeystrokeFeed</a>



<a href="https://msdn.microsoft.com/6bdca5cc-84b4-4184-a8cc-76dddc573b35">ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed
      </a>
 

 

