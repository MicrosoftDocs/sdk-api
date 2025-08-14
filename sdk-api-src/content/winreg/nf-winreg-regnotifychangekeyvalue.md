---
UID: NF:winreg.RegNotifyChangeKeyValue
title: RegNotifyChangeKeyValue function (winreg.h)
description: Notifies the caller about changes to the attributes or contents of a specified registry key.
helpviewer_keywords: ["REG_NOTIFY_CHANGE_ATTRIBUTES","REG_NOTIFY_CHANGE_LAST_SET","REG_NOTIFY_CHANGE_NAME","REG_NOTIFY_CHANGE_SECURITY","REG_NOTIFY_THREAD_AGNOSTIC","RegNotifyChangeKeyValue","RegNotifyChangeKeyValue function","_win32_regnotifychangekeyvalue","base.regnotifychangekeyvalue","winreg/RegNotifyChangeKeyValue"]
old-location: base\regnotifychangekeyvalue.htm
tech.root: winprog
ms.assetid: aad72ed5-1123-4a8b-9fc4-b54a713b635e
ms.date: 12/05/2018
ms.keywords: REG_NOTIFY_CHANGE_ATTRIBUTES, REG_NOTIFY_CHANGE_LAST_SET, REG_NOTIFY_CHANGE_NAME, REG_NOTIFY_CHANGE_SECURITY, REG_NOTIFY_THREAD_AGNOSTIC, RegNotifyChangeKeyValue, RegNotifyChangeKeyValue function, _win32_regnotifychangekeyvalue, base.regnotifychangekeyvalue, winreg/RegNotifyChangeKeyValue
req.header: winreg.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegNotifyChangeKeyValue
 - winreg/RegNotifyChangeKeyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - Kernel32.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegNotifyChangeKeyValue
---

# RegNotifyChangeKeyValue function


## -description

Notifies the caller about changes to the attributes or contents of a specified registry key.

## -parameters

### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>
This parameter must be a local handle. If 
<b>RegNotifyChangeKeyValue</b> is called with a remote handle, it returns ERROR_INVALID_HANDLE.

The key must have been opened with the KEY_NOTIFY access right. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param bWatchSubtree [in]

If this parameter is TRUE, the function reports changes in the specified key and its subkeys. If the parameter is <b>FALSE</b>, the function reports changes only in the specified key.

### -param dwNotifyFilter [in]

A value that indicates the changes that should be reported. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_NAME"></a><a id="reg_notify_change_name"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_NAME</b></dt>
<dt>0x00000001L</dt>
</dl>
</td>
<td width="60%">
Notify the caller if a subkey is added or deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_ATTRIBUTES"></a><a id="reg_notify_change_attributes"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_ATTRIBUTES</b></dt>
<dt>0x00000002L</dt>
</dl>
</td>
<td width="60%">
Notify the caller of changes to the attributes of the key, such as the security descriptor information.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_LAST_SET"></a><a id="reg_notify_change_last_set"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_LAST_SET</b></dt>
<dt>0x00000004L</dt>
</dl>
</td>
<td width="60%">
Notify the caller of changes to a value of the key. This can include adding or deleting a value, or changing an existing value.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_CHANGE_SECURITY"></a><a id="reg_notify_change_security"></a><dl>
<dt><b>REG_NOTIFY_CHANGE_SECURITY</b></dt>
<dt>0x00000008L</dt>
</dl>
</td>
<td width="60%">
Notify the caller of changes to the security descriptor of the key.

</td>
</tr>
<tr>
<td width="40%"><a id="REG_NOTIFY_THREAD_AGNOSTIC"></a><a id="reg_notify_thread_agnostic"></a><dl>
<dt><b>REG_NOTIFY_THREAD_AGNOSTIC</b></dt>
<dt>0x10000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that the lifetime of the registration must not be tied to the lifetime of the thread issuing the <b>RegNotifyChangeKeyValue</b> call.

<div class="alert"><b>Note</b>  This flag value is only supported in Windows 8 and later.</div>
<div> </div>
</td>
</tr>
</table>

### -param hEvent [in, optional]

A handle to an event. If the <i>fAsynchronous</i> parameter is <b>TRUE</b>, the function returns immediately and changes are reported by signaling this event. If <i>fAsynchronous</i> is <b>FALSE</b>, <i>hEvent</i> is ignored.

### -param fAsynchronous [in]

If this parameter is <b>TRUE</b>, the function returns immediately and reports changes by signaling the specified event. If this parameter is <b>FALSE</b>, the function does not return until a change has occurred. 




If <i>hEvent</i> does not specify a valid event, the <i>fAsynchronous</i> parameter cannot be <b>TRUE</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

This function detects a single change. After the caller receives a notification event, it should call the function again to receive the next notification.

<div class="alert"><b>Note</b>  On Windows NT, Windows 2000, and Windows XP calling <b>RegNotifyChangeKeyValue</b> for a particular key handle causes change notifications to continue to occur for as long as the key handle is valid. This causes a second call to <b>RegNotifyChangeKeyValue</b> to return immediately, if any changes have occurred in the interim period between the first and second calls. If the API is being used asynchronously, the passed event handle will be signaled immediately if any interim changes have occurred.</div>
<div> </div>
This function cannot be used to detect changes to the registry that result from using the <a href="/windows/desktop/api/winreg/nf-winreg-regrestorekeya">RegRestoreKey</a> function.

If the specified key is closed, the event is signaled. This means that an application should not depend on the key being open after returning from a wait operation on the event.

The <b>REG_NOTIFY_THREAD_AGNOSTIC</b> flag introduced in Windows 8 enables the use of <b>RegNotifyChangeKeyValue</b> for ThreadPool threads.

If the thread that called 
<b>RegNotifyChangeKeyValue</b> exits, the event is signaled. To continue to monitor additional changes in the value of the key, call 
<b>RegNotifyChangeKeyValue</b> again from another thread.
				

With the exception of <b>RegNotifyChangeKeyValue</b> calls with <b>REG_NOTIFY_THREAD_AGNOSTIC</b> set, this function must be called on persistent threads. If the calling thread is from a thread pool and it is not persistent, the event is signaled every time the thread terminates, not just when there is a registry change. To ensure accurate results, run the thread pool work in a persistent thread by using the <a href="/windows/desktop/api/winbase/nf-winbase-setthreadpoolcallbackpersistent">SetThreadpoolCallbackPersistent</a> function, or create your own thread using the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>  function. (For the original thread pool API, specify WT_EXECUTEINPERSISTENTTHREAD using the <a href="/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem">QueueUserWorkItem</a> function.) 

This function should not be called multiple times with the same  value for the <i>hKey</i> but different values for the <i>bWatchSubtree</i> and <i>dwNotifyFilter</i> parameters. The function will succeed but the changes will be ignored. To change the  
watch parameters, you must first close the key handle by calling 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>, reopen the key handle by calling 
<a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, and then call <b>RegNotifyChangeKeyValue</b> with the new parameters. 

Each time a process calls <b>RegNotifyChangeKeyValue</b> with the same set of parameters, it establishes another wait operation, creating a resource leak. Therefore, check that you are not calling <b>RegNotifyChangeKeyValue</b> with the same parameters until the previous wait operation has completed.

To monitor registry operations in more detail, see <a href="/windows/desktop/ETW/registry">Registry</a>.

<b>Windows XP/2000:  </b>When <b>RegNotifyChangeKeyValue</b> is called for a particular key handle, change notifications occur for as long as the key handle is valid. This causes a second call to <b>RegNotifyChangeKeyValue</b> to return immediately, if any changes occur in the interim between the first and second calls. If the function is being used asynchronously, the passed event handle will be signaled immediately if any changes occur in the interim. 


#### Examples

The following program illustrates how to use <b>RegNotifyChangeKeyValue</b>.


```cpp
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

//void main(int argc, char *argv[])
void __cdecl _tmain(int argc, TCHAR *argv[])
{
   DWORD  dwFilter = REG_NOTIFY_CHANGE_NAME |
                     REG_NOTIFY_CHANGE_ATTRIBUTES |
                     REG_NOTIFY_CHANGE_LAST_SET |
                     REG_NOTIFY_CHANGE_SECURITY; 

   HANDLE hEvent;
   HKEY   hMainKey;
   HKEY   hKey;
   LONG   lErrorCode;

   // Display the usage error message.
   if (argc != 3) 
   {
      _tprintf(TEXT("Usage: notify [HKLM|HKU|HKCU|HKCR|HCC] [<subkey>]\n"));
      return;
   }

   // Convert parameters to appropriate handles.
   if (_tcscmp(TEXT("HKLM"), argv[1]) == 0) hMainKey=HKEY_LOCAL_MACHINE;
   else if(_tcscmp(TEXT("HKU"), argv[1]) == 0) hMainKey=HKEY_USERS;
   else if(_tcscmp(TEXT("HKCU"), argv[1]) == 0) hMainKey=HKEY_CURRENT_USER;
   else if(_tcscmp(TEXT("HKCR"), argv[1]) == 0) hMainKey=HKEY_CLASSES_ROOT;
   else if(_tcscmp(TEXT("HCC"), argv[1]) == 0) hMainKey=HKEY_CURRENT_CONFIG;
   else 
   {
      _tprintf(TEXT("Usage: notify [HKLM|HKU|HKCU|HKCR|HCC] [<subkey>]\n"));
      return;
   }

   // Open a key.
    lErrorCode = RegOpenKeyEx(hMainKey, argv[2], 0, KEY_NOTIFY, &hKey);
   if (lErrorCode != ERROR_SUCCESS)
   {
      _tprintf(TEXT("Error in RegOpenKeyEx (%d).\n"), lErrorCode);
      return;
   }

   // Create an event.
   hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
   if (hEvent == NULL)
   {
      _tprintf(TEXT("Error in CreateEvent (%d).\n"), GetLastError());
      return;
   }

   // Watch the registry key for a change of value.
   lErrorCode = RegNotifyChangeKeyValue(hKey, 
                                        TRUE, 
                                        dwFilter, 
                                        hEvent, 
                                        TRUE);
   if (lErrorCode != ERROR_SUCCESS)
   {
      _tprintf(TEXT("Error in RegNotifyChangeKeyValue (%d).\n"), lErrorCode);
      return;
   }

   // Wait for an event to occur.
   _tprintf(TEXT("Waiting for a change in the specified key...\n"));
   if (WaitForSingleObject(hEvent, INFINITE) == WAIT_FAILED)
   {
      _tprintf(TEXT("Error in WaitForSingleObject (%d).\n"), GetLastError());
      return;
   }
   else _tprintf(TEXT("\nChange has occurred.\n"));

   // Close the key.
   lErrorCode = RegCloseKey(hKey);
   if (lErrorCode != ERROR_SUCCESS)
   {
      _tprintf(TEXT("Error in RegCloseKey (%d).\n"), GetLastError());
      return;
   }
   
   // Close the handle.
   if (!CloseHandle(hEvent))
   {
      _tprintf(TEXT("Error in CloseHandle.\n"));
      return;
   }
}

```

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumkeyexa">RegEnumKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regenumvaluea">RegEnumValue</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryinfokeya">RegQueryInfoKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa">RegQueryValueEx</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>