---
UID: NF:msajtransport.AllJoynCloseBusHandle
title: AllJoynCloseBusHandle function (msajtransport.h)
author: windows-sdk-content
description: Closes the Named Pipe handle.
old-location: alljoyn\alljoynclosebushandle.htm
tech.root: AllJoyn
ms.assetid: FE545239-F88D-4876-8A3F-52AC8CA63FBB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AllJoynCloseBusHandle, AllJoynCloseBusHandle function [AllJoyn API], alljoyn.alljoynclosebushandle, msajtransport/AllJoynCloseBusHandle
ms.topic: function
req.header: msajtransport.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: MSAJApi.lib
req.dll: MSAJApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MSAJApi.dll
api_name:
 - AllJoynCloseBusHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AllJoynCloseBusHandle function


## -description


Closes the Named Pipe handle.


## -parameters




### -param busHandle [in]

The bus handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



