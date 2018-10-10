---
UID: NS:ddeml.tagCONVCONTEXT
title: tagCONVCONTEXT
author: windows-sdk-content
description: Contains information supplied by a Dynamic Data Exchange (DDE) client application. The information is useful for specialized or cross-language DDE conversations.
old-location: dataxchg\convcontext_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\convcontext.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "*PCONVCONTEXT, CONVCONTEXT, CONVCONTEXT structure [Data Exchange], PCONVCONTEXT, PCONVCONTEXT structure pointer [Data Exchange], _win32_CONVCONTEXT_str, _win32_convcontext_str_cpp, dataxchg.convcontext_str, ddeml/CONVCONTEXT, ddeml/PCONVCONTEXT, tagCONVCONTEXT, winui._win32_convcontext_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddeml.h
req.include-header: Windows.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - CONVCONTEXT
product: Windows
targetos: Windows
req.typenames: CONVCONTEXT, *PCONVCONTEXT
req.redist: 
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
For added security, your application can specify a security code with the <b>dwSecurity</b> member. The application could then examine this value in the <a href="https://msdn.microsoft.com/en-us/library/ms648742(v=VS.85).aspx">DdeCallback</a> function to check the identity of the client application. However, a value that is hard-coded into an application might be discovered. Thus, you may want to provide the security code in some other way, such as through user input.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>
 

 

