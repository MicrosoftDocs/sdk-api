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

# tagCONVCONTEXT structure


## -description


Contains information supplied by a Dynamic Data Exchange (DDE) client application. The information is useful for specialized or cross-language DDE conversations. 


## -struct-fields




### -field cb

Type: <b>UINT</b>

The structure's size, in bytes. 


### -field wFlags

Type: <b>UINT</b>

The conversation context flags. Currently, no flags are defined for this member. 


### -field wCountryID

Type: <b>UINT</b>

The country/region code identifier for topic-name and item-name strings. 


### -field iCodePage

Type: <b>int</b>

The code page for topic-name and item-name strings. Non-multilingual clients should set this member to <b>CP_WINANSI</b>. Unicode clients should set this value to <b>CP_WINUNICODE</b>. 
					


### -field dwLangID

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/8a6373e0-46c2-4b1b-bc67-543f426ef15a">language identifier</a> for topic-name and item-name strings. 


### -field dwSecurity

Type: <b>DWORD</b>

A private (application-defined) security code. 


### -field qos

Type: <b><a href="https://msdn.microsoft.com/21f99d04-b21b-442c-9034-35f9f7bbee53">SECURITY_QUALITY_OF_SERVICE</a></b>

The quality of service a DDE client wants from the system during a given conversation. The quality of service level specified lasts for the duration of the conversation. It cannot be changed once the conversation is started. 


## -remarks



<h3><a id="Security_Warning"></a><a id="security_warning"></a><a id="SECURITY_WARNING"></a>Security Warning</h3>
For added security, your application can specify a security code with the <b>dwSecurity</b> member. The application could then examine this value in the <a href="https://msdn.microsoft.com/bf982432-9b08-4dba-9b7a-b9c135022488">DdeCallback</a> function to check the identity of the client application. However, a value that is hard-coded into an application might be discovered. Thus, you may want to provide the security code in some other way, such as through user input.




## -see-also




<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>
 

 

