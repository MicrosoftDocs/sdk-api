---
UID: NF:wtsapi32.WTSCloseServer
title: WTSCloseServer function (wtsapi32.h)
author: windows-sdk-content
description: Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtscloseserver.htm
tech.root: TermServ
ms.assetid: 092a6107-21bf-40a7-9fe7-f069eb0c89ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WTSCloseServer, WTSCloseServer function [Remote Desktop Services], _win32_wtscloseserver, termserv.wtscloseserver, wtsapi32/WTSCloseServer
ms.topic: function
f1_keywords: 
 - "wtsapi32/WTSCloseServer"
dev_langs:
 - c++
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
api_name:
 - WTSCloseServer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WTSCloseServer function


## -description


Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server opened by a call to the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function.

Do not pass <b>WTS_CURRENT_SERVER_HANDLE</b> for this parameter.


## -returns



This function does not return a value.




## -remarks



Call the <b>WTSCloseServer</b> function as part of your program's clean-up routine to 
    close all the server handles opened by calls to the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenserverexa">WTSOpenServerEx</a> function.

After the handle has been closed, it cannot be used with any other WTS APIs.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>
 

 

