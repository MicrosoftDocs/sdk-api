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

# NdrGetUserMarshalInfo function


## -description


The 
<b>NdrGetUserMarshalInfo</b> function provides additional information to wire_marshal and user_marshal helper functions.


## -parameters




### -param pFlags

Pointer by the same name that RPC passed to the helper function.


### -param InformationLevel

Desired level of detail to be received. Different levels imply different sets of information fields. Only level 1 is currently defined.


### -param pMarshalInfo

Address of a memory buffer, supplied by the application, to receive the requested information. The buffer must be at least as large as the information structure indicated by <i>InformationLevel</i>.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
At least one of the arguments was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_INVALID_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Current marshaling buffer was not valid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>NdrGetUserMarshalInfo</b> function is called by the <b>wire_marshal</b> or <b>user_marshal</b> helper functions (provided by the application) &lt;<i>type</i>&gt;<b>_UserSize</b>, &lt;<i>type</i>&gt;<b>_UserMarshal</b>, &lt;<i>type</i>&gt;<b>_UserUnmarshal</b>, and &lt;<i>type</i>&gt;<b>_UserFree</b> to receive extra information about the state of the call. A common use for this function is to obtain the size of the marshaling buffer for the purpose of checking for end of buffer conditions. Sending incorrectly sized data is a commonly used method of breaching system security.

For a full listing of the information returned by 
<b>NdrGetUserMarshalInfo</b>, see 
<a href="https://msdn.microsoft.com/3c7b4cd4-fb72-40a6-9450-4edf82cade2c">NDR_USER_MARSHAL_INFO</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c7b4cd4-fb72-40a6-9450-4edf82cade2c">NDR_USER_MARSHAL_INFO</a>



<a href="midl.user_marshal">user_marshal</a>



<a href="midl.wire_marshal">wire_marshal</a>
 

 

