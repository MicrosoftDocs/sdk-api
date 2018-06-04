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

# IdnToNameprepUnicode function


## -description


Converts an internationalized domain name (IDN) or another internationalized label to the NamePrep form specified by Network Working Group <a href="http://go.microsoft.com/fwlink/p/?linkid=161552">RFC 3491</a>, but does not perform the additional conversion to Punycode. For more information and links to related draft standards, see <a href="https://msdn.microsoft.com/e0ca356e-f8c1-4845-ae1e-ce2ae8987515">Handling Internationalized Domain Names (IDNs)</a>.


## -parameters




### -param dwFlags [in]

Flags specifying conversion options. For detailed definitions, see the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/e39aa5c2-3f76-40b2-9948-bbd795c6c525">IdnToAscii</a>.


### -param lpUnicodeCharStr [in]

Pointer to a Unicode string representing an IDN or another internationalized label.


### -param cchUnicodeChar [in]

Count of Unicode characters in the input Unicode string indicated by <i>lpUnicodeCharStr</i>.


### -param lpNameprepCharStr [out, optional]

Pointer to a buffer that receives a version of the input Unicode string converted through NamePrep processing. Alternatively, the function can retrieve <b>NULL</b> for this parameter, if <i>cchNameprepChar</i> is set to 0. In this case, the function returns the size required for this buffer.


### -param cchNameprepChar [in]

Size, in characters, of the buffer indicated by <i>lpNameprepCharStr</i>. The application can set the size to 0 to retrieve <b>NULL</b> in <i>lpNameprepCharStr</i> and have the function return the required buffer size.


## -returns



Returns the number of characters retrieved in <i>lpNameprepCharStr</i> if successful. The retrieved string is null-terminated only if the input Unicode string is null-terminated.

If the function succeeds and the value of <i>cchNameprepChar</i> is 0, the function returns the required size, in characters including a terminating null character if it was part of the input buffer.

The function returns 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_NAME. An invalid name was supplied to the function. Note that this error code catches all syntax errors. </li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string.</li>
</ul>



## -remarks



See Remarks for <a href="https://msdn.microsoft.com/e39aa5c2-3f76-40b2-9948-bbd795c6c525">IdnToAscii</a>. 	  	 
		


#### Examples


<a href="https://msdn.microsoft.com/9739efa5-8b88-4f9c-983d-806968caf9d5">NLS: Internationalized Domain Name (IDN) Conversion Sample</a> demonstrates the use of this function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e0ca356e-f8c1-4845-ae1e-ce2ae8987515">Handling Internationalized Domain Names (IDNs)</a>



<a href="https://msdn.microsoft.com/e39aa5c2-3f76-40b2-9948-bbd795c6c525">IdnToAscii</a>



<a href="https://msdn.microsoft.com/90707414-aef7-4265-bc2b-d48ac79db099">IdnToUnicode</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>
 

 

