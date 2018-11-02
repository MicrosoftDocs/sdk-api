---
UID: NF:recapis.IsStringSupported
title: IsStringSupported function
author: windows-sdk-content
description: Returns a value that indicates whether a word, date, time, number, or other text that is passed in is contained in the dictionary.The results of this test depend on the factoid setting.
old-location: tablet\isstringsupported.htm
tech.root: tablet
ms.assetid: b646225a-0008-45f3-9c42-48adf4942ebd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IsStringSupported, IsStringSupported function [Tablet PC], b646225a-0008-45f3-9c42-48adf4942ebd, recapis/IsStringSupported, tablet.isstringsupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - IsStringSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsStringSupported function


## -description



Returns a value that indicates whether a word, date, time, number, or other text that is passed in is contained in the dictionary.

The results of this test depend on the factoid setting.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param wcString

The count, in Unicode (wide) characters, of <i>pwcString</i>.


### -param pwcString

The Unicode (wide) characters to test.


## -returns



This function can return one of these values.

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
Success.

This function also returns S_OK if the recognizer does not support this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The string is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 




## -remarks



This function is optional.

The results of this test depend on the factoid setting. For example, if the factoid setting is set to default, then "hello","555-1234", and "10/19/2002" all return S_OK. However, if the factoid is set to TELEPHONE, only "555-1234" returns S_OK, the others return S_FALSE. For more information about factoids, see <a href="https://msdn.microsoft.com/9d5fc370-ba58-438b-8850-f31f0f0f6608">Supported Factoids from Version 1</a>.

Note that this function should take into consideration any information specified in <a href="https://msdn.microsoft.com/f5461326-3def-4564-81ea-32a63b889da0">SetTextContext</a> when returning a value. For example, if the recognizer receives calls to SetTextContext ("http:", "") and receives a URL factoid, SetFactoid ((!IS_URL)) then IsStringSupported("www.microsoft.com") should return S_FALSE because it is missing the "//".

The COERCE flag has no effect on IsStringSupported.



