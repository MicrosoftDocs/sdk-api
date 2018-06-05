---
UID: NF:wtsapi32.WTSOpenServerA
title: WTSOpenServerA function
author: windows-sdk-content
description: Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtsopenserver.htm
old-project: TermServ
ms.assetid: f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: WTSOpenServer, WTSOpenServer function [Remote Desktop Services], WTSOpenServerA, WTSOpenServerW, _win32_wtsopenserver, termserv.wtsopenserver, wtsapi32/WTSOpenServer, wtsapi32/WTSOpenServerA, wtsapi32/WTSOpenServerW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSOpenServerW (Unicode) and WTSOpenServerA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wtsapi32.dll
api_name:
-	WTSOpenServer
-	WTSOpenServerA
-	WTSOpenServerW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSOpenServerA function


## -description


Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param pServerName [in]

Pointer to a null-terminated string specifying the NetBIOS name of the RD Session Host server.


## -returns



If the function succeeds, the return value is a handle to the specified server.

If the function fails, it returns a handle that is not valid. You can test the validity of the handle by using it in another function call.




## -remarks



When you have finished using the handle returned by 
<b>WTSOpenServer</b>, release it by calling the <a href="https://msdn.microsoft.com/092a6107-21bf-40a7-9fe7-f069eb0c89ca">WTSCloseServer</a> function.

You do not need to open a handle for operations performed on the RD Session Host server on which your application is running. Use the constant <b>WTS_CURRENT_SERVER_HANDLE</b> instead.




## -see-also




<a href="https://msdn.microsoft.com/092a6107-21bf-40a7-9fe7-f069eb0c89ca">WTSCloseServer</a>
 

 

