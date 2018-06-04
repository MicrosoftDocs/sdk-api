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

# IWSManSession::Invoke


## -description


Invokes a method and  returns the results of the method call.


## -parameters




### -param actionUri [in]

The URI of the method to invoke.


### -param resourceUri [in]

The identifier of the resource to invoke a method.

This parameter can contain one of the following:

<ul>
<li>URI with or without <a href="windows_remote_management_glossary.htm">selectors</a>.</li>
<li>
<a href="https://msdn.microsoft.com/0904b7eb-d4ce-46a7-bf58-452e7c0d41e9">ResourceLocator</a> object which may contain selectors,  <a href="windows_remote_management_glossary.htm">fragments</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/dn965779">options</a>.</li>
<li><a href="windows_remote_management_glossary.htm">WS-Addressing</a> endpoint reference as described in the WS-Management protocol  standard.  For more information about the public specification for the WS-Management protocol, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84316">Management Specifications Index Page</a>.</li>
</ul>

### -param parameters [in]

An XML representation of the input for the method. This string must be supplied or this method will fail.


### -param flags [in, optional]

Reserved for future use. Must be set to 0.


### -param result [out]

An XML representation of the method output.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>



<a href="https://msdn.microsoft.com/c83d0631-2efb-47d9-abcf-ab0c8de06c36">Session.Invoke</a>
 

 

