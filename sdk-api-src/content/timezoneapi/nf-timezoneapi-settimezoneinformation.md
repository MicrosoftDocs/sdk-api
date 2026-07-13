---
UID: NF:timezoneapi.SetTimeZoneInformation
title: SetTimeZoneInformation function (timezoneapi.h)
description: Sets the current time zone settings. These settings control translations from Coordinated Universal Time (UTC) to local time.
helpviewer_keywords: ["SetTimeZoneInformation","SetTimeZoneInformation function","_win32_settimezoneinformation","base.settimezoneinformation","timezoneapi/SetTimeZoneInformation"]
old-location: base\settimezoneinformation.htm
tech.root: winprog
ms.assetid: afb13501-3a87-433a-a05e-139103060109
ms.date: 12/05/2018
ms.keywords: SetTimeZoneInformation, SetTimeZoneInformation function, _win32_settimezoneinformation, base.settimezoneinformation, timezoneapi/SetTimeZoneInformation
req.header: timezoneapi.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetTimeZoneInformation
 - timezoneapi/SetTimeZoneInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-timezone-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-TimeZone-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetTimeZoneInformation
---

# SetTimeZoneInformation function


## -description

Sets the current time zone settings. These settings control translations from Coordinated Universal Time (UTC) to local time.

To support boundaries for daylight saving time that change from year to year, use the <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a> function.

## -parameters

### -param lpTimeZoneInformation [in]

A pointer to a 
<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure that contains the new settings.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application must have the SE_TIME_ZONE_NAME privilege for this function to succeed. This privilege is disabled by default. Use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function to enable the privilege before calling 
<b>SetTimeZoneInformation</b>, and then to disable the privilege after the 
<b>SetTimeZoneInformation</b> call. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>The application must have the SE_SYSTEMTIME_NAME privilege.

> [!IMPORTANT]
> Starting with Windows Vista and Windows Server 2008 through all current versions of Windows, call <b><a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a></b> instead of <b>SetTimeZoneInformation</b> to set system time zone information.  <b>SetDynamicTimeZoneInformation</b> supports the full history of changes to standard time and daylight saving time provided by the dynamic data in the Windows registry.  If an application uses <b>SetTimeZoneInformation</b>, dynamic daylight saving time support is disabled for the system and the message "Your current time zone is not recognized. Please select a valid time zone." will appear to the user in the Windows time zone settings.

To inform Explorer that the time zone has changed, send the 
<a href="/windows/desktop/winmsg/wm-settingchange">WM_SETTINGCHANGE</a> message.

All translations between UTC and local time are based on the following formula:

UTC = local time + bias

The bias is the difference, in minutes, between UTC and local time.


#### Examples

The following example displays the current time zone, then adjusts the time zone one zone west. The old and new  time zone names are displayed. You can also verify the changes using Date and Time in Control Panel. The new name is displayed on the <b>Date&amp;Time</b> tab as the <b>Current Time Zone</b>. The new time zone is displayed in the drop-down list on the <b>Time Zone</b> tab. To undo these changes, simply choose your old time zone from the drop-down list.


```cpp
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <string.h>
#include <strsafe.h>

int main()
{
   TIME_ZONE_INFORMATION tziOld, tziNew, tziTest;
   DWORD dwRet;

   // Enable the required privilege

   HANDLE hToken;
   TOKEN_PRIVILEGES tkp;

   OpenProcessToken(GetCurrentProcess(), TOKEN_ADJUST_PRIVILEGES|TOKEN_QUERY, &hToken);
   LookupPrivilegeValue(NULL, SE_TIME_ZONE_NAME, &tkp.Privileges[0].Luid);
   tkp.PrivilegeCount = 1;
   tkp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, (PTOKEN_PRIVILEGES)NULL, 0);

   // Retrieve the current time zone information

   dwRet = GetTimeZoneInformation(&tziOld);

   if(dwRet == TIME_ZONE_ID_STANDARD || dwRet == TIME_ZONE_ID_UNKNOWN)    
      wprintf(L"%s\n", tziOld.StandardName);
   else if( dwRet == TIME_ZONE_ID_DAYLIGHT )
      wprintf(L"%s\n", tziOld.DaylightName);
   else
   {
      printf("GTZI failed (%d)\n", GetLastError());
      return 0;
   }

   // Adjust the time zone information

   ZeroMemory(&tziNew, sizeof(tziNew));
   tziNew.Bias = tziOld.Bias + 60;
   StringCchCopy(tziNew.StandardName, 32, L"Test Standard Zone");
   tziNew.StandardDate.wMonth = 10;
   tziNew.StandardDate.wDayOfWeek = 0;
   tziNew.StandardDate.wDay = 5;
   tziNew.StandardDate.wHour = 2;

   StringCchCopy(tziNew.DaylightName, 32, L"Test Daylight Zone");
   tziNew.DaylightDate.wMonth = 4;
   tziNew.DaylightDate.wDayOfWeek = 0;
   tziNew.DaylightDate.wDay = 1;
   tziNew.DaylightDate.wHour = 2;
   tziNew.DaylightBias = -60;

   if( !SetTimeZoneInformation( &tziNew ) ) 
   {
      printf("STZI failed (%d)\n", GetLastError());
      return 0;
   }

   // Retrieve and display the newly set time zone information

   dwRet = GetTimeZoneInformation(&tziTest);

   if(dwRet == TIME_ZONE_ID_STANDARD || dwRet == TIME_ZONE_ID_UNKNOWN)    
      wprintf(L"%s\n", tziTest.StandardName);
   else if( dwRet == TIME_ZONE_ID_DAYLIGHT )
      wprintf(L"%s\n", tziTest.DaylightName);
   else printf("GTZI failed (%d)\n", GetLastError());

   // Disable the privilege

   tkp.Privileges[0].Attributes = 0; 
   AdjustTokenPrivileges(hToken, FALSE, &tkp, 0, (PTOKEN_PRIVILEGES) NULL, 0); 

   return 1;
}

```

## -see-also

<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation">GetTimeZoneInformation</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation">SetDynamicTimeZoneInformation</a>



<a href="/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>