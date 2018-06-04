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

# NetWkstaTransportDel function


## -description


<p class="CCE_Message">[This function is obsolete. To change the default settings for transport protocols manually, use the <b>Local Area Connection Properties</b> dialog box in the <b>Network and Dial-Up Connections</b> folder.]

Not supported.

The 
				<b>NetWkstaTransportDel</b> function unbinds the transport protocol from the redirector. (The redirector is the software on the client computer that generates file requests to the server computer.)


## -parameters




### -param OPTIONAL

TBD


### -param transportname [in]

Pointer to a string that specifies the name of the transport protocol to disconnect from the redirector.


### -param ucond [in]

Specifies the level of force to use when disconnecting the transport protocol from the redirector. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USE_NOFORCE"></a><a id="use_noforce"></a><dl>
<dt><b>USE_NOFORCE</b></dt>
</dl>
</td>
<td width="60%">
Fail the disconnection if open files exist on the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_FORCE"></a><a id="use_force"></a><dl>
<dt><b>USE_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Fail the disconnection if open files exist on the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_LOTS_OF_FORCE"></a><a id="use_lots_of_force"></a><dl>
<dt><b>USE_LOTS_OF_FORCE</b></dt>
</dl>
</td>
<td width="60%">
Close any open files and delete the connection.

</td>
</tr>
</table>
 


#### - servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 


This string must begin with \\.
					


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UseNotFound</b></dt>
</dl>
</td>
<td width="60%">
The network connection does not exist.

</td>
</tr>
</table>
 




## -remarks



Only members of the Administrators local group can successfully execute the 
<b>NetWkstaTransportDel</b> function.



