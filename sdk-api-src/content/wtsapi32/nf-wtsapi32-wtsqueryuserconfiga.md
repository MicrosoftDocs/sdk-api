---
UID: NF:wtsapi32.WTSQueryUserConfigA
title: WTSQueryUserConfigA function (wtsapi32.h)
description: Retrieves configuration information for the specified user on the specified domain controller or Remote Desktop Session Host (RD Session Host) server. (ANSI)
helpviewer_keywords: ["WTSQueryUserConfigA", "wtsapi32/WTSQueryUserConfigA"]
old-location: termserv\wtsqueryuserconfig.htm
tech.root: TermServ
ms.assetid: aabbcc03-3241-49ab-ab11-ccd3e6893e78
ms.date: 12/05/2018
ms.keywords: WTSQueryUserConfig, WTSQueryUserConfig function [Remote Desktop Services], WTSQueryUserConfigA, WTSQueryUserConfigW, _win32_wtsqueryuserconfig, termserv.wtsqueryuserconfig, wtsapi32/WTSQueryUserConfig, wtsapi32/WTSQueryUserConfigA, wtsapi32/WTSQueryUserConfigW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSQueryUserConfigA
 - wtsapi32/WTSQueryUserConfigA
dev_langs:
 - c++
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
---

# WTSQueryUserConfigA function


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
<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_class">WTS_CONFIG_CLASS</a> enumeration type. The documentation for 
<b>WTS_CONFIG_CLASS</b> describes the format of the data returned in <i>ppBuffer</i> for each of the information types.

### -param ppBuffer [out]

Pointer to a variable that receives a pointer to the requested information. The format and contents of the data depend on the information class specified in the <i>WTSConfigClass</i> parameter. To free the returned buffer, call the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a> function.

### -param pBytesReturned [out]

Pointer to a variable that receives the size, in bytes, of the data returned in <i>ppBuffer</i>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>WTSQueryUserConfig</b> and 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a> functions are passed a server name instead of a handle because user account information often resides on a domain controller. To set user configuration information, use the primary domain controller. You can call the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetdcname">NetGetDCName</a> function to get the name of the primary domain controller. To query user configuration information, you can use the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetanydcname">NetGetAnyDCName</a> function to get the name of a primary or backup domain controller.

Any domain controller can set or query user configuration information. Use the 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function to retrieve the name of a domain controller.





> [!NOTE]
> The wtsapi32.h header defines WTSQueryUserConfig as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememory">WTSFreeMemory</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssetuserconfiga">WTSSetUserConfig</a>



<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_class">WTS_CONFIG_CLASS</a>
