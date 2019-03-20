---
UID: NF:winreg.RegOverridePredefKey
title: RegOverridePredefKey function (winreg.h)
author: windows-sdk-content
description: Maps a predefined registry key to the specified registry key.
old-location: base\regoverridepredefkey.htm
tech.root: SysInfo
ms.assetid: ad58b7ff-cd61-4719-9028-b470ae7e9bb0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegOverridePredefKey, RegOverridePredefKey function, _win32_regoverridepredefkey, base.regoverridepredefkey, winreg/RegOverridePredefKey
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegOverridePredefKey function


## -description


Maps a predefined registry key to the specified registry key.


## -parameters




### -param hKey [in]

A handle to one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>: 




<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_CONFIG</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_PERFORMANCE_DATA</b>
<b>HKEY_USERS</b>

### -param hNewHKey [in, optional]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> or <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function. It cannot be one of the predefined keys. The function maps <i>hKey</i> to refer to the <i>hNewHKey</i> key. This affects only the calling process. 




If <i>hNewHKey</i> is <b>NULL</b>, the function restores the default mapping of the predefined key.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



The 
<b>RegOverridePredefKey</b> function is intended for software installation programs. It allows them to remap a predefined key, load a DLL component that will be installed on the system, call an entry point in the DLL, and examine the changes to the registry that the component attempted to make. The installation program can then write those changes to the locations intended by the DLL, or make changes to the data before writing it.

For example, consider an installation program that installs an ActiveX control as part of an application installation. The installation program needs to call the control's 
<a href="https://msdn.microsoft.com/en-us/library/ms682162(v=VS.85).aspx">DllRegisterServer</a> entry point to enable the control to register itself. Before this call, the installation program can call 
<b>RegOverridePredefKey</b> to remap <b>HKEY_CLASSES_ROOT</b> to a temporary key such as <b>HKEY_CURRENT_USER</b>\<b><i>TemporaryInstall</i></b>\<b><i>DllRegistration</i></b>. It then calls <b>DllRegisterServer</b>, which causes the ActiveX control to write its registry entries to the temporary key. The installation program then calls 
<b>RegOverridePredefKey</b> again to restore the original mapping of <b>HKEY_CLASSES_ROOT</b>. The installation program can modify the keys written to the temporary key, if necessary, before copying them to the original <b>HKEY_CLASSES_ROOT</b>.

After the call to 
<b>RegOverridePredefKey</b>, you can safely call 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> to close the <i>hNewHKey</i> handle. The system maintains its own reference to <i>hNewHKey</i>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms682162(v=VS.85).aspx">DllRegisterServer</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

