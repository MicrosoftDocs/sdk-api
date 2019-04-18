---
UID: NF:wtsapi32.WTSQueryUserConfigW
title: WTSQueryUserConfigW function (wtsapi32.h)
author: windows-sdk-content
description: Retrieves configuration information for the specified user on the specified domain controller or Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wtsqueryuserconfig.htm
tech.root: TermServ
ms.assetid: aabbcc03-3241-49ab-ab11-ccd3e6893e78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WTSQueryUserConfig, WTSQueryUserConfig function [Remote Desktop Services], WTSQueryUserConfigA, WTSQueryUserConfigW, _win32_wtsqueryuserconfig, termserv.wtsqueryuserconfig, wtsapi32/WTSQueryUserConfig, wtsapi32/WTSQueryUserConfigA, wtsapi32/WTSQueryUserConfigW
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSQueryUserConfigW (Unicode) and WTSQueryUserConfigA (ANSI)
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
 - WTSQueryUserConfig
 - WTSQueryUserConfigA
 - WTSQueryUserConfigW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WTSQueryUserConfigW function


## -description


Retrieves configuration information for the specified user on the specified domain controller or Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param pServerName [in]

Pointer to a null-terminated string containing the name of a domain controller or an RD Session Host server. Specify <b>WTS_CURRENT_SERVER_NAME</b> to indicate the RD Session Host server on which your application is running.


### -param pUserName [in]

Pointer to a null-terminated string containing the user name to query. To retrieve the default user settings for the RD Session Host server, set this parameter to <b>NULL</b>.

<b>Windows Server 2008 and Windows Vista:  </b>Setting this parameter to <b>NULL</b> returns an error.


### -param WTSConfigClass [in]

Specifies the type of information to retrieve. This parameter can be one of the values from the 
<a href="https://msdn.microsoft.com/623b8a86-aa0d-497c-a2e6-5526f9b13d98">WTS_CONFIG_CLASS</a> enumeration type. The documentation for 
<b>WTS_CONFIG_CLASS</b> describes the format of the data returned in <i>ppBuffer</i> for each of the information types.


### -param ppBuffer [out]

Pointer to a variable that receives a pointer to the requested information. The format and contents of the data depend on the information class specified in the <i>WTSConfigClass</i> parameter. To free the returned buffer, call the 
<a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a> function.


### -param pBytesReturned [out]

Pointer to a variable that receives the size, in bytes, of the data returned in <i>ppBuffer</i>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>WTSQueryUserConfig</b> and 
<a href="https://msdn.microsoft.com/44d027c6-6ebb-4750-a0fa-17fdf31e45cd">WTSSetUserConfig</a> functions are passed a server name instead of a handle because user account information often resides on a domain controller. To set user configuration information, use the primary domain controller. You can call the 
<a href="https://msdn.microsoft.com/3e32aacc-088e-455a-bc1b-92274e98d2e5">NetGetDCName</a> function to get the name of the primary domain controller. To query user configuration information, you can use the 
<a href="https://msdn.microsoft.com/64dacbf4-46c2-4f82-b250-b7d338535e7c">NetGetAnyDCName</a> function to get the name of a primary or backup domain controller.

Any domain controller can set or query user configuration information. Use the 
<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> function to retrieve the name of a domain controller.




## -see-also




<a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a>



<a href="https://msdn.microsoft.com/44d027c6-6ebb-4750-a0fa-17fdf31e45cd">WTSSetUserConfig</a>



<a href="https://msdn.microsoft.com/623b8a86-aa0d-497c-a2e6-5526f9b13d98">WTS_CONFIG_CLASS</a>
 

 

