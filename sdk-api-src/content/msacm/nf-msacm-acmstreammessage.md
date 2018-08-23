---
UID: NF:msacm.acmStreamMessage
title: acmStreamMessage function
author: windows-sdk-content
description: The acmStreamMessage function sends a driver-specific message to an ACM driver.
old-location: multimedia\acmstreammessage.htm
old-project: Multimedia
ms.assetid: 30f77126-a874-4014-bbde-ce194da2c61c
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "_win32_acmStreamMessage, acmStreamMessage, acmStreamMessage function [Windows Multimedia], msacm/acmStreamMessage, multimedia.acmstreammessage"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msacm.h
req.include-header: 
req.redist: 
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmStreamMessage
product: Windows
targetos: Windows
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
req.product: GDI+ 1.1
---

# acmStreamMessage function


## -description



The <b>acmStreamMessage</b> function sends a driver-specific message to an ACM driver.




## -parameters




### -param has

Handle to an open conversion stream.


### -param uMsg

Message to send.


### -param lParam1

Message parameter.


### -param lParam2

Message parameter.


## -returns



Returns the value returned by the ACM device driver.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

