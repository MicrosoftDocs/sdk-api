---
UID: NS:ws2spi.WSPData
title: WSPData
author: windows-sdk-content
description: The WSPDATA structure contains service provider information.
old-location: winsock\wspdata_2.htm
old-project: winsock
ms.assetid: 0592aa8f-5fac-4bbd-9fb8-e61d374ad0a6
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPWSPDATA, LPWSPDATA, LPWSPDATA structure pointer [Winsock], WSPDATA, WSPDATA structure [Winsock], WSPData, _win32_wspdata_2, winsock.wspdata_2, ws2spi/LPWSPDATA, ws2spi/WSPDATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ws2spi.h
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
tech.root: 
req.typenames: WSPDATA, *LPWSPDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2spi.h
api_name:
 - WSPDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSPData structure


## -description



			The 
<b>WSPDATA</b> structure contains service provider information.


## -struct-fields




### -field wVersion

Version of the Windows Sockets SPI specification that the Windows Sockets service provider expects the caller to use.


### -field wHighVersion

Highest version of the Windows Sockets SPI specification that this service provider can support (also encoded as above). Normally this will be the same as <b>wVersion</b>.


### -field szDescription

Null-terminated Unicode string into which the Windows Sockets provider copies a description of itself. The text (up to 256 characters in length) can contain any characters except control and formatting characters: the most likely use to which an SPI client will put this is to display it (possibly truncated) in a status message.


## -see-also




<a href="https://msdn.microsoft.com/9ebfe81c-bed6-4bde-b1dd-5eaefbaac9cf">WSPStartup</a>
 

 

