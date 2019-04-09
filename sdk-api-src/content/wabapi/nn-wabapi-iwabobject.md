---
UID: NN:wabapi.IWABObject
title: IWABObject (wabapi.h)
author: windows-sdk-content
description: Do not use. This interface provides access to the Windows Address Book (WAB) object which contains function pointers to memory allocation functions and database maintenance functions.
old-location: wab\_wab_IWABObject.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\iwabobject.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWABObject, IWABObject interface [Windows Address Book], IWABObject interface [Windows Address Book],described, _wab_IWABObject, wab._wab_IWABObject, wabapi/IWABObject
ms.topic: interface
req.header: wabapi.h
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
req.dll: Wab32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IWABObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IWABObject interface


## -description


Do not use. This interface provides access to the  Windows Address Book (WAB) object which contains function pointers to memory allocation functions and database maintenance functions. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWABObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWABObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWABObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629459(v=VS.85).aspx">AllocateBuffer</a>
</td>
<td align="left" width="63%">
Allocates memory for buffers that are passed to 
		WAB methods.  The buffer must be freed with 
		<a href="https://msdn.microsoft.com/en-us/library/ms629463(v=VS.85).aspx">FreeBuffer</a>, and may be reallocated with 
		<a href="https://msdn.microsoft.com/en-us/library/ms629460(v=VS.85).aspx">AllocateMore</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629460(v=VS.85).aspx">AllocateMore</a>
</td>
<td align="left" width="63%">
Allocates a memory buffer that is linked to another buffer 
		previously allocated with the 
		<a href="https://msdn.microsoft.com/en-us/library/ms629459(v=VS.85).aspx">AllocateBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629461(v=VS.85).aspx">Backup</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629462(v=VS.85).aspx">Find</a>
</td>
<td align="left" width="63%">
Launches the WAB Find dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629463(v=VS.85).aspx">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees memory allocated with 
		<a href="https://msdn.microsoft.com/en-us/library/ms629459(v=VS.85).aspx">AllocateBuffer</a> or any of the other 
		WAB methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629464(v=VS.85).aspx">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629465(v=VS.85).aspx">GetMe</a>
</td>
<td align="left" width="63%">
Retrieves the entry identifier of the object that has been designated 
		as "ME."

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629466(v=VS.85).aspx">Import</a>
</td>
<td align="left" width="63%">
Imports a .wab file into the user's Address Book.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629468(v=VS.85).aspx">LDAPUrl</a>
</td>
<td align="left" width="63%">
Processes an LDAP URL 
		and displays the results obtained from the URL. 
		If the URL only contains a server name, 
		the WAB launches the Find window with the server name 
		filled in. If the URL contains an 
		LDAP query, the query is processed. If the query has 
		a single result, the WAB shows details about the result; 
		if the query has multiple results, the WAB shows the Find 
		dialog box with multiple search results filled in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629469(v=VS.85).aspx">SetMe</a>
</td>
<td align="left" width="63%">
Designates a particular contact as the ME object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629470(v=VS.85).aspx">VCardCreate</a>
</td>
<td align="left" width="63%">
Translates the properties of a given MailUser object into a 
		vCard file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629471(v=VS.85).aspx">VCardDisplay</a>
</td>
<td align="left" width="63%">
Displays properties on a vCard file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629472(v=VS.85).aspx">VCardRetrieve</a>
</td>
<td align="left" width="63%">
Reads a vCard file and creates a MailUser object containing 
		the vCard properties.

</td>
</tr>
</table> 

