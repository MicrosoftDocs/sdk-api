---
UID: NF:winreg.RegOverridePredefKey
title: RegOverridePredefKey function (winreg.h)

description: Maps a predefined registry key to the specified registry key.
old-location: base\regoverridepredefkey.htm
tech.root: SysInfo
ms.assetid: ad58b7ff-cd61-4719-9028-b470ae7e9bb0

ms.date: 12/05/2018
ms.keywords: RegOverridePredefKey, RegOverridePredefKey function, _win32_regoverridepredefkey, base.regoverridepredefkey, winreg/RegOverridePredefKey
ms.topic: function
f1_keywords: 
 - "winreg/RegOverridePredefKey"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegOverridePredefKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegOverridePredefKey function


## -description


Maps a predefined registry key to the specified registry key.


## -parameters




### -param hKey [in]

A handle to one of the following 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/predefined-keys">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_PERFORMANCE_DATA</b>
<b>HKEY_USERS</b>

### -param hNewHKey [in, optional]

A handle to an open registry key. This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a> or <a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a> function. It cannot be one of the predefined keys. The function maps <i>hKey</i> to refer to the <i>hNewHKey</i> key. This affects only the calling process. 




If <i>hNewHKey</i> is <b>NULL</b>, the function restores the default mapping of the predefined key.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



The 
<b>RegOverridePredefKey</b> function is intended for software installation programs. It allows them to remap a predefined key, load a DLL component that will be installed on the system, call an entry point in the DLL, and examine the changes to the registry that the component attempted to make. The installation program can then write those changes to the locations intended by the DLL, or make changes to the data before writing it.

For example, consider an installation program that installs an ActiveX control as part of an application installation. The installation program needs to call the control's 
<a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> entry point to enable the control to register itself. Before this call, the installation program can call 
<b>RegOverridePredefKey</b> to remap <b>HKEY_CLASSES_ROOT</b> to a temporary key such as <b>HKEY_CURRENT_USER</b>\<b><i>TemporaryInstall</i></b>\<b><i>DllRegistration</i></b>. It then calls <b>DllRegisterServer</b>, which causes the ActiveX control to write its registry entries to the temporary key. The installation program then calls 
<b>RegOverridePredefKey</b> again to restore the original mapping of <b>HKEY_CLASSES_ROOT</b>. The installation program can modify the keys written to the temporary key, if necessary, before copying them to the original <b>HKEY_CLASSES_ROOT</b>.

After the call to 
<b>RegOverridePredefKey</b>, you can safely call 
<a href="https://docs.microsoft.com/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> to close the <i>hNewHKey</i> handle. The system maintains its own reference to <i>hNewHKey</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/registry">Registry Overview</a>
 

 

