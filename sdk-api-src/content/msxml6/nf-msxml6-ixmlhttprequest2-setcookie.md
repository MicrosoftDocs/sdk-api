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

# IXMLHTTPRequest2::SetCookie


## -description


Sets a cookie associated with the specified URL in the HTTP cookie jar.


## -parameters




### -param pCookie

A pointer to an <a href="https://msdn.microsoft.com/208829B0-DBCC-4C22-910D-D6826283F8A0">XHR_COOKIE</a> structure that specifies the cookie and properties of the cookie to be associated with  the specified URL.


### -param pdwCookieState

A pointer to a value that indicates the cookie state if the call completes successfully. 

This parameter can be one of the values from the <a href="https://msdn.microsoft.com/040a5ae8-ec18-44a6-a3e9-376637cc005a">XHR_COOKIE_STATE</a> enumeration type defined in the <i>Msxml6.h</i>  header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_UNKNOWN"></a><a id="xhr_cookie_state_unknown"></a><dl>
<dt><b>XHR_COOKIE_STATE_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Reserved.



</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_ACCEPT"></a><a id="xhr_cookie_state_accept"></a><dl>
<dt><b>XHR_COOKIE_STATE_ACCEPT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The cookie was accepted.



</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_PROMPT"></a><a id="xhr_cookie_state_prompt"></a><dl>
<dt><b>XHR_COOKIE_STATE_PROMPT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The user is prompted to accept or refuse the cookie.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_LEASH"></a><a id="xhr_cookie_state_leash"></a><dl>
<dt><b>XHR_COOKIE_STATE_LEASH</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The cookie is accepted only in the first-party context.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_DOWNGRADE"></a><a id="xhr_cookie_state_downgrade"></a><dl>
<dt><b>XHR_COOKIE_STATE_DOWNGRADE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The cookie was accepted and became session cookie.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_REJECT"></a><a id="xhr_cookie_state_reject"></a><dl>
<dt><b>XHR_COOKIE_STATE_REJECT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The cookie was rejected.



</td>
</tr>
</table>
 


## -returns



Returns <b>S_OK</b> on success.




## -remarks



The <b>SetCookie</b> method has different behavior for Windows Store apps and Windows desktop applications. 

When used in a Windows Store app, the <b>SetCookie</b> method  by default sets the cookie as a persistent cookie in the Windows Store app. When the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/208829B0-DBCC-4C22-910D-D6826283F8A0">XHR_COOKIE</a> has the <b>XHR_COOKIE_IS_SESSION</b> flag set, then the cookie is set only for the current session of the app.

When used in a Windows desktop application, the <b>SetCookie</b> method  by default sets a persistent cookie that  is system wide and shared by all Windows desktop applications.   When the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/208829B0-DBCC-4C22-910D-D6826283F8A0">XHR_COOKIE</a> has the <b>XHR_COOKIE_IS_SESSION</b> flag set, then the cookie is set only for the current session of the Windows desktop application.




## -see-also




<a href="https://msdn.microsoft.com/A2A9C54B-92A2-41EA-A741-797BA219BCDA">GetCookie Method</a>



<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/208829B0-DBCC-4C22-910D-D6826283F8A0">XHR_COOKIE Structure</a>



<a href="https://msdn.microsoft.com/040a5ae8-ec18-44a6-a3e9-376637cc005a">XHR_COOKIE_STATE</a>
 

 

