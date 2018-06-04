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

# IWMReaderAdvanced4::AddLogParam


## -description



The <b>AddLogParam</b> method adds a named value to the logging information that the reader object will send to the sever.




## -parameters




### -param wszNameSpace [in]

Optional wide-character string that contains the namespace for the log entry. This parameter can be <b>NULL</b>. Namespace names are limited to 1024 wide characters.


### -param wszName [in]

Wide-character string that contains the name of the log entry. Log entry names are limited to 1024 wide characters.


### -param wszValue [in]

Wide-character string that contains the value of the log entry. Log entry values are limited to 1024 wide characters.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters exceeded the allowed string length.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



The reader object sends logging data to the server in the form of an XML stream. The <b>AddLogParam</b> method enables the client to specify additional logging entries. The <i>wszNameSpace</i> parameter can be used to specify an XML namespace for the new entry. If you do not specify a namespace, the default namespace is used. However, the reader will not override log entries already defined by the server, with the following exception: If the server specifies an empty string ("") for the cs-media-role or cs-media-name entry, you can overwrite these entries. By default, a server running Windows Media Services 9 Series sends an empty string for cs-media-role, and the name of the file for cs-media-name.

To send the logging information to the server, call the <b>SendLogParams</b> method. To retrieve the log entries on the server, you must provide a custom logging plug-in, using the Windows Media Services 9 Series SDK. The default logging plug-in writes just the W3C-compliant log summary, so custom log entries are not included in the log.




## -see-also




<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/3b345573-bdca-4a1f-b272-716e2ca4c88c">IWMReaderAdvanced4::SendLogParams</a>
 

 

