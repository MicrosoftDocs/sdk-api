---
UID: NN:wabapi.IWABObject
title: IWABObject
author: windows-sdk-content
description: Do not use. This interface provides access to the Windows Address Book (WAB) object which contains function pointers to memory allocation functions and database maintenance functions.
old-location: wab\_wab_IWABObject.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\ifaces\iwabobject\iwabobject.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWABObject, IWABObject interface [Windows Address Book], IWABObject interface [Windows Address Book],described, _wab_IWABObject, wab._wab_IWABObject, wabapi/IWABObject
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">AllocateBuffer</a>
</td>
<td align="left" width="63%">
Allocates memory for buffers that are passed to 
		WAB methods.  The buffer must be freed with 
		<a href="https://msdn.microsoft.com/ded42aaf-8ed0-4e21-9905-37629d2919a1">FreeBuffer</a>, and may be reallocated with 
		<a href="https://msdn.microsoft.com/f36171ce-7059-4a07-ad74-e3c092128821">AllocateMore</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f36171ce-7059-4a07-ad74-e3c092128821">AllocateMore</a>
</td>
<td align="left" width="63%">
Allocates a memory buffer that is linked to another buffer 
		previously allocated with the 
		<a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">AllocateBuffer</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cb21701-9a1f-4248-96e0-6d35d72b1afa">Backup</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79609e9b-5286-48ca-b95c-79bcfd847b0a">Find</a>
</td>
<td align="left" width="63%">
Launches the WAB Find dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ded42aaf-8ed0-4e21-9905-37629d2919a1">FreeBuffer</a>
</td>
<td align="left" width="63%">
Frees memory allocated with 
		<a href="https://msdn.microsoft.com/59c4362a-2a03-47a0-a606-e8be3be22d28">AllocateBuffer</a> or any of the other 
		WAB methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce330dfa-d58e-4ded-9bf2-1fc207fea55b">GetLastError</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46dec97d-4dd4-4f27-8b04-59340d4cce83">GetMe</a>
</td>
<td align="left" width="63%">
Retrieves the entry identifier of the object that has been designated 
		as "ME."

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88676a07-8b03-4ed3-a5bb-a54a11b093c8">Import</a>
</td>
<td align="left" width="63%">
Imports a .wab file into the user's Address Book.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96694de8-6b8f-4498-a218-0d157ee50d3b">LDAPUrl</a>
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
<a href="https://msdn.microsoft.com/3ba8c4d4-97c0-4d05-b83b-3e0b62dbea05">SetMe</a>
</td>
<td align="left" width="63%">
Designates a particular contact as the ME object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e03a86c-ea41-4046-8e2b-611a03e57c96">VCardCreate</a>
</td>
<td align="left" width="63%">
Translates the properties of a given MailUser object into a 
		vCard file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c68a87a-741e-44aa-970b-614a029a47b3">VCardDisplay</a>
</td>
<td align="left" width="63%">
Displays properties on a vCard file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91897c36-769f-41b1-8133-652e58ce2ef9">VCardRetrieve</a>
</td>
<td align="left" width="63%">
Reads a vCard file and creates a MailUser object containing 
		the vCard properties.

</td>
</tr>
</table> 

