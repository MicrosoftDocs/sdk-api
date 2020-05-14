---
UID: NF:winbase.GetCurrentHwProfileW
title: GetCurrentHwProfileW function (winbase.h)
description: Retrieves information about the current hardware profile for the local computer.helpviewer_keywords: ["GetCurrentHwProfile","GetCurrentHwProfile function","GetCurrentHwProfileA","GetCurrentHwProfileW","_win32_getcurrenthwprofile","base.getcurrenthwprofile","winbase/GetCurrentHwProfile","winbase/GetCurrentHwProfileA","winbase/GetCurrentHwProfileW"]
old-location: base\getcurrenthwprofile.htm
tech.root: SysInfo
ms.assetid: 152067bb-3896-43ef-a882-12a159f92cc7
ms.date: 12/05/2018
ms.keywords: GetCurrentHwProfile, GetCurrentHwProfile function, GetCurrentHwProfileA, GetCurrentHwProfileW, _win32_getcurrenthwprofile, base.getcurrenthwprofile, winbase/GetCurrentHwProfile, winbase/GetCurrentHwProfileA, winbase/GetCurrentHwProfileW
f1_keywords:
- winbase/GetCurrentHwProfile
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCurrentHwProfileW (Unicode) and GetCurrentHwProfileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-hwprof-l1-1-0.dll
api_name:
- GetCurrentHwProfile
- GetCurrentHwProfileA
- GetCurrentHwProfileW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentHwProfileW function


## -description


Retrieves information about the current hardware profile for the local computer.


## -parameters




### -param lpHwProfileInfo [out]

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-hw_profile_infoa">HW_PROFILE_INFO</a> structure that receives information about the current hardware profile.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>GetCurrentHwProfile</b> function retrieves the display name and globally unique identifier (GUID) string for the hardware profile. The function also retrieves the reported docking state for portable computers with docking stations.

The system generates a GUID for each hardware profile and stores it as a string in the registry. You can use 
<b>GetCurrentHwProfile</b> to retrieve the GUID string to use as a registry subkey under your application's configuration settings key in <b>HKEY_CURRENT_USER</b>. This enables you to store each user's settings for each hardware profile. For example, the Colors control panel application could use the subkey to store each user's color preferences for different hardware profiles, such as profiles for the docked and undocked states. Applications that use this functionality can check the current hardware profile when they start up, and update their settings accordingly.

Applications can also update their settings when a system device message, such as 
<a href="https://docs.microsoft.com/windows/desktop/DevIO/dbt-configchanged">DBT_CONFIGCHANGED</a>, indicates that the hardware profile has changed.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void main(void) 
{
   HW_PROFILE_INFO   HwProfInfo;
   if (!GetCurrentHwProfile(&HwProfInfo)) 
   {
      _tprintf(TEXT("GetCurrentHwProfile failed with error %lx\n"), 
                 GetLastError());
      return;
   }
   _tprintf(TEXT("DockInfo = %d\n"), HwProfInfo.dwDockInfo);
   _tprintf(TEXT("Profile Guid = %s\n"), HwProfInfo.szHwProfileGuid);
   _tprintf(TEXT("Friendly Name = %s\n"), HwProfInfo.szHwProfileName);
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevIO/dbt-configchanged">DBT_CONFIGCHANGED</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-hw_profile_infoa">HW_PROFILE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
 

 

