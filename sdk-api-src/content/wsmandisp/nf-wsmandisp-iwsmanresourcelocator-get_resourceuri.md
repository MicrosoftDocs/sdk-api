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

# IWSManResourceLocator::get_ResourceURI


## -description


The <a href="windows_remote_management_glossary.htm">resource URI</a> of the requested resource. This property can contain only the path, not a query string for specific instances.

This property is read/write.


## -parameters


## -remarks




<a href="https://msdn.microsoft.com/0904b7eb-d4ce-46a7-bf58-452e7c0d41e9">ResourceLocator</a> is the corresponding scripting object for the <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> interface.

The following is an example of a proper path for  <b>ResourceURI</b>.

<pre class="syntax" xml:space="preserve"><code>"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"</code></pre>
The following path does not work because it  contains a key for a specific instance. Use the <a href="https://msdn.microsoft.com/2f6c1169-8e2a-4919-9a1a-856dbe41a9ce">IWSManResourceLocator::AddSelector</a> method to specify a particular instance.

<pre class="syntax" xml:space="preserve"><code>"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"</code></pre>
The corresponding scripting method is <a href="https://msdn.microsoft.com/adb1e08a-290f-4a23-a6e4-d7567a6b7eee">ResourceLocator.ResourceURI</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>



<a href="https://msdn.microsoft.com/adb1e08a-290f-4a23-a6e4-d7567a6b7eee">ResourceLocator.ResourceURI</a>
 

 

