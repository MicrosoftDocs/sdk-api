---
UID: NF:isolatedwindowsenvironmentutils.IsProcessInIsolatedWindowsEnvironment
tech.root: security
title: IsProcessInIsolatedWindowsEnvironment
ms.date: 03/09/2023
targetos: Windows
description: Determines in which execution environment the application is running.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: isolatedwindowsenvironmentutils.dll
req.header: isolatedwindowsenvironmentutils.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: IsolatedWindowsEnvironmentUtils.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - isolatedwindowsenvironmentutils.dll
api_name:
 - IsProcessInIsolatedWindowsEnvironment
f1_keywords:
 - IsProcessInIsolatedWindowsEnvironment
 - isolatedwindowsenvironmentutils/IsProcessInIsolatedWindowsEnvironment
dev_langs:
 - c++
helpviewer_keywords:
 - IsProcessInIsolatedWindowsEnvironment
---

## -description

Determines in which execution environment the application is running – a host or an Isolated Environment.

## -parameters

### -param isProcessInIsolatedWindowsEnvironment

`[out]`

A pointer to a boolean value that receives the result of the API. This parameter will be `true` if the process is in an Isolated Windows Environment, `false` otherwise.

## -returns

Returns `S_OK` if the function succeeds. If it fails, it returns an `HRESULT` error code.

## -remarks

Any application using [Microsoft Defender Application Guard (MDAG)](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview) will require the ability to find which execution environment it is running in. This is needed so that the app can behave appropriately to protect user/enterprise data, user identity, and the business interests of the app.

#### Examples

The following example shows how to use the `IsProcessInIsolatedWindowsEnvironment` API to determine the execution environment of the app.

```cpp
#define PrintInfo wprintf

typedef HRESULT (*pIsProcessInIsolatedWindowsEnvironment)
                  (_Out_ BOOL *isProcessInIsolatedWindowsEnvironment);

int PrintError(unsigned int line, HRESULT hr)
{
  wprintf_s(L"ERROR: Line:%d HRESULT: 0x%X\n", line, hr);
  return hr;
}

HRESULT TakeActionAsPerExecutionEnvironment()
{
  //For instance the action could be saving changes to user settings for the app.
  //Lets assume the app has made a design decision to save change to user settings if
  //the app is running on the host, and discard the changes to user settings if they were
  //changed in an Isolated Environment.

  HMODULE dllInstance (LoadLibrary(L"IsolatedWindowsEnvironmentUtils.dll"));

  if (nullptr == dllInstance)
  {
    PrintInfo(L" Cannot load the library IsolatedWindowsEnvironmentUtils.dll \n");
    return E_FAIL;
  }

  auto pfn = reinterpret_cast<pIsProcessInIsolatedWindowsEnvironment>

  (GetProcAddress(dllInstance, "IsProcessInIsolatedWindowsEnvironment"));

  if (nullptr == pfn)
  {
    PrintInfo(L"Function definition IsProcessInIsolatedWindowsEnvironment() is not found.\n");
    FreeLibrary(dllInstance);
    return E_FAIL;
  }

  BOOL isInIsolatedWindowsEnvironment = FALSE;

  HRESULT hr = pfn(&isInIsolatedWindowsEnvironment);

  if (FAILED(hr))
  {
    FreeLibrary(dllInstance);
    return PrintError(__LINE__, hr);
  }

  if (isInIsolatedWindowsEnvironment == TRUE) //app is running in Isolated Environment
  {
    //do not save changes to the app’s user settings in this case
    PrintInfo(L"Discarding changes to app’s user settings.\n");

    //<TO-DO-Start>
    //Add app specific custom logic here
    //<TO-DO-End>
  }
  else
  {
    //Save changes to the app’s user settings in this case
    PrintInfo(L"Saving changes to app’s user settings.\n");

    //<TO-DO-Start>
    //Add app specific custom logic here
    //<TO-DO-End>
  }

  FreeLibrary(dllInstance);
  return S_OK;
}
```

## -see-also

[Microsoft Defender Application Guard overview](/windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview)

[IsolatedWindowsEnvironment](/uwp/api/windows.security.isolation.isolatedwindowsenvironment)

[IsolatedWindowsEnvironmentHost](/uwp/api/windows.security.isolation.isolatedwindowsenvironmenthost)
