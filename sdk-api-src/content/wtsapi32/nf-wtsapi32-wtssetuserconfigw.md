---
UID: NF:wtsapi32.WTSSetUserConfigW
title: WTSSetUserConfigW function (wtsapi32.h)
description: Modifies configuration information for the specified user on the specified domain controller or Remote Desktop Session Host (RD Session Host) server. (Unicode)
helpviewer_keywords: ["WTSSetUserConfig", "WTSSetUserConfig function [Remote Desktop Services]", "WTSSetUserConfigW", "_win32_wtssetuserconfig", "termserv.wtssetuserconfig", "wtsapi32/WTSSetUserConfig", "wtsapi32/WTSSetUserConfigW"]
old-location: termserv\wtssetuserconfig.htm
tech.root: TermServ
ms.assetid: 44d027c6-6ebb-4750-a0fa-17fdf31e45cd
ms.date: 12/05/2018
ms.keywords: WTSSetUserConfig, WTSSetUserConfig function [Remote Desktop Services], WTSSetUserConfigA, WTSSetUserConfigW, _win32_wtssetuserconfig, termserv.wtssetuserconfig, wtsapi32/WTSSetUserConfig, wtsapi32/WTSSetUserConfigA, wtsapi32/WTSSetUserConfigW
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSSetUserConfigW (Unicode) and WTSSetUserConfigA (ANSI)
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
 - WTSSetUserConfigW
 - wtsapi32/WTSSetUserConfigW
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
 - WTSSetUserConfig
 - WTSSetUserConfigA
 - WTSSetUserConfigW
---

# WTSSetUserConfigW function


## -description

Modifies configuration information for the specified user on the specified domain controller or 
    Remote Desktop Session Host (RD Session Host) server.

## -parameters

### -param pServerName [in]

Pointer to a null-terminated string containing the name of a domain controller or 
      RD Session Host server. Specify <b>WTS_CURRENT_SERVER_NAME</b> to indicate the 
      RD Session Host server on which your application is running.

### -param pUserName [in]

Pointer to a null-terminated string containing the name of the user whose configuration is being set.

### -param WTSConfigClass [in]

Specifies the type of information to set for the user. This parameter can be one of the values from the 
      <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_class">WTS_CONFIG_CLASS</a> enumeration type. The 
      documentation for <b>WTS_CONFIG_CLASS</b> describes 
      the format of the data specified in <i>ppBuffer</i> for each of the information types.

### -param pBuffer [in]

Pointer to the data used to modify the specified user's configuration.

### -param DataLength [in]

Size, in <b>TCHARs</b>, of the <i>pBuffer</i> buffer.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a> and 
    <b>WTSSetUserConfig</b> functions are passed a server 
    name instead of a handle because user account information often resides on a domain controller. To set user 
    configuration information, use the primary domain controller. You can call the 
    <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetdcname">NetGetDCName</a> function to get the name of the primary 
    domain controller. To query user configuration information, you can use the 
    <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetanydcname">NetGetAnyDCName</a> function to get the name of a 
    primary or backup domain controller.

Any domain controller can set or query user configuration information. Use the 
    <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function to retrieve the name of a domain 
    controller.

If the value of the  <i>WTSConfigClass</i> parameter corresponds to an integer value in the 
     <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_class">WTS_CONFIG_CLASS</a> enumeration, define the value 
     to be set as a <b>DWORD</b>.  Then cast the value to an <b>LPWSTR</b> 
     in the call to <b>WTSSetUserConfig</b>, as in the 
     following example:


```cpp
WTSSetUserConfig( strServer.GetBuffer(0), 
                  m_strName.GetBuffer(0), 
                  WTSUserConfigfAllowLogonTerminalServer, 
                  (LPWSTR) &dwEnable, 
                  sizeof(DWORD));
```






> [!NOTE]
> The wtsapi32.h header defines WTSSetUserConfig as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsqueryuserconfiga">WTSQueryUserConfig</a>



<a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_config_class">WTS_CONFIG_CLASS</a>
