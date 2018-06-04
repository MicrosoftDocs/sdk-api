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

# IWMHeaderInfo::AddScript


## -description



The <b>AddScript</b> method adds a script, consisting of type and command strings, and a specific time, to the header section of the ASF file. 




## -parameters




### -param pwszType [in]

Pointer to a wide-character null-terminated string containing the type. Script types are limited to 1024 wide characters.


### -param pwszCommand [in]

Pointer to a wide-character null-terminated string containing the command. Script commands are limited to 10240 wide characters.


### -param cnsScriptTime [in]

The script time in 100-nanosecond increments.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No value was supplied in <i>pwszType</i> or <i>pwszCommand</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer parameter does not contain a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



Before <b>BeginWriting</b> has been called, the writer only supports <b>AddScript</b>. The reader does not support <b>AddScript</b>, and always returns E_NOTIMPL.

You should not add a large number of script commands to the file header if the file is intended for streaming. Some protocols impose limits on the size of a header. Limits differ by protocol, but if your script commands total tens of kilobytes, you should create a script stream instead.

When using DRM to encrypt a file, no script command can have a presentation time of 0.




## -see-also




<a href="https://msdn.microsoft.com/649f9a73-c70a-4524-b577-366ade969f2f">IWMHeaderInfo Interface</a>



<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/779a7618-9f22-4caf-8a4e-b622e422c30d">IWMHeaderInfo::GetScript</a>



<a href="https://msdn.microsoft.com/c66e808d-25f9-4745-8bcc-731f2556f470">IWMHeaderInfo::RemoveScript</a>



<a href="https://msdn.microsoft.com/be8a2d22-35cb-4b8d-ad00-e8a45bb85b39">Using Script Commands</a>
 

 

