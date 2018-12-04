---
UID: NF:msctf.ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed
title: ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed
author: windows-sdk-content
description: ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed method
old-location: tsf\itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed.htm
tech.root: TSF
ms.assetid: 6bdca5cc-84b4-4184-a8cc-76dddc573b35
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DisableSystemKeystrokeFeed, DisableSystemKeystrokeFeed method [Text Services Framework], DisableSystemKeystrokeFeed method [Text Services Framework],ITfConfigureSystemKeystrokeFeed interface, ITfConfigureSystemKeystrokeFeed interface [Text Services Framework],DisableSystemKeystrokeFeed method, ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed, ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed, _tsf_itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed_ref, msctf/ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed, tsf.itfconfiguresystemkeystrokefeed_disablesystemkeystrokefeed
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
 - ITfConfigureSystemKeystrokeFeed.DisableSystemKeystrokeFeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfConfigureSystemKeystrokeFeed::DisableSystemKeystrokeFeed


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
</table>
 




## -remarks



By default, the TSF manager will process keystrokes and pass them to the text services. An application prevents this by calling this method. Typically, this method is called when text service input is inappropriate, for example when a menu is displayed.

Calls to this method are cumulative, so every call to this method requires a subsequent call to <a href="https://msdn.microsoft.com/66dc5db3-c4d9-422e-bbc0-300409a9576a">ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed</a>.




## -see-also




<a href="https://msdn.microsoft.com/9b15d628-87aa-4e20-b9c3-fb29a79683cb">ITfConfigureSystemKeystrokeFeed</a>



<a href="https://msdn.microsoft.com/66dc5db3-c4d9-422e-bbc0-300409a9576a">ITfConfigureSystemKeystrokeFeed::EnableSystemKeystrokeFeed
      </a>
 

 

