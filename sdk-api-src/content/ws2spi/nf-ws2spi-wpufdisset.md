---
UID: NF:ws2spi.WPUFDIsSet
title: WPUFDIsSet function
author: windows-driver-content
description: The WPUFDIsSet function checks the membership of the specified socket handle.
old-location: winsock\wpufdisset_2.htm
old-project: WinSock
ms.assetid: 87726b13-ede4-4c73-be98-4ad4180ea3e7
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: WPUFDIsSet, WPUFDIsSet function [Winsock], _win32_wpufdisset_2, winsock.wpufdisset_2, ws2spi/WPUFDIsSet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ws2spi.h
api_name:
-	WPUFDIsSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WPUFDIsSet function


## -description



			The 
<b>WPUFDIsSet</b> function checks the membership of the specified socket handle.


## -parameters




### -param s [in]

Descriptor identifying the socket.


### -param fdset

TBD




#### - set [in]

Set to check for the membership of socket <i>s</i>.


## -returns




						If no error occurs, a value of nonzero is returned denoting that socket <i>s</i> is a member of the <i>set</i> parameter. Otherwise, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/a8f2922d-2474-406d-b1c7-631f05ccdd9c">WSPSelect</a>
 

 

