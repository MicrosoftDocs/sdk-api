---
UID: NF:winreg.RegOpenUserClassesRoot
title: RegOpenUserClassesRoot function
author: windows-sdk-content
description: Retrieves a handle to the HKEY_CLASSES_ROOT key for a specified user. The user is identified by an access token.
old-location: base\regopenuserclassesroot.htm
tech.root: sysinfo
ms.assetid: bd068826-cf88-4fc7-a7d6-96cc03e923c7
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: RegOpenUserClassesRoot, RegOpenUserClassesRoot function, _win32_regopenuserclassesroot, base.regopenuserclassesroot, winreg/RegOpenUserClassesRoot
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - API-MS-Win-Core-Localregistry-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Registry-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - api-ms-win-core-registry-l1-1-1.dll
api_name:
 - RegOpenUserClassesRoot
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegOpenUserClassesRoot function


## -description


Retrieves a handle to the <b>HKEY_CLASSES_ROOT</b> key for a specified user. The user is identified by an access token. The returned key has a view of the registry that merges the contents of the <b>HKEY_LOCAL_MACHINE</b>\Software\Classes key with the contents of the Software\Classes keys in the user's registry hive. For more information, see 
<a href="https://msdn.microsoft.com/b404875f-11e1-48f2-98d2-0378a0646ed3">HKEY_CLASSES_ROOT Key</a>.


## -parameters




### -param hToken [in]

A handle to a primary or impersonation access token that identifies the user of interest. This can be a token handle returned by a call to 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, 
<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, 
<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, 
<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>, 
<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or 
<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> functions. 




The handle must have TOKEN_QUERY access. For more information, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param dwOptions

This parameter is reserved and must be zero.


### -param samDesired [in]

A mask that specifies the desired access rights to the key. The function fails if the security descriptor of the key does not permit the requested access for the calling process. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. When you no longer need the returned handle, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function to close it.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



The 
<b>RegOpenUserClassesRoot</b> function enables you to retrieve the merged <b>HKEY_CLASSES_ROOT</b> information for users other than the interactive user. For example, the server component of a client/server application could use 
<b>RegOpenUserClassesRoot</b> to retrieve the merged information for a client.

<b>RegOpenUserClassesRoot</b> fails if the user profile for the specified user is not loaded. When a user logs on interactively, the system automatically loads the user's profile. For other users, you can call the 
<a href="_shell_loaduserprofile">LoadUserProfile</a> function to load the user's profile. However, <b>LoadUserProfile</b> can be very time-consuming, so do not call it for this purpose unless it is absolutely necessary to have the user's merged <b>HKEY_CLASSES_ROOT</b> information.

Applications running in the security context of the interactively logged-on user do not need to use 
<b>RegOpenUserClassesRoot</b>. These applications can call the 
<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a> function to retrieve a merged view of the <b>HKEY_CLASSES_ROOT</b> key for the interactive user.




## -see-also




<a href="_shell_loaduserprofile">LoadUserProfile</a>



<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

