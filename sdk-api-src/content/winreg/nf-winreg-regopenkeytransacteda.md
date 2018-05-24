---
UID: NF:winreg.RegOpenKeyTransactedA
title: RegOpenKeyTransactedA function
author: windows-driver-content
description: Opens the specified registry key and associates it with a transaction.
old-location: base\regopenkeytransacted.htm
old-project: SysInfo
ms.assetid: 11663ed2-d17c-4f08-be7b-9b591271fbcd
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: RegOpenKeyTransacted, RegOpenKeyTransacted function, RegOpenKeyTransactedA, RegOpenKeyTransactedW, base.regopenkeytransacted, winreg/RegOpenKeyTransacted, winreg/RegOpenKeyTransactedA, winreg/RegOpenKeyTransactedW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winreg.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegOpenKeyTransactedW (Unicode) and RegOpenKeyTransactedA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PERF_OBJECT_TYPE, *PPERF_OBJECT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-Core-Registry-l2-1-0.dll
-	advapi32legacy.dll
-	API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
-	RegOpenKeyTransacted
-	RegOpenKeyTransactedA
-	RegOpenKeyTransactedW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegOpenKeyTransactedA function


## -description


Opens the specified registry key and associates it with a  transaction. Note that key names are not case sensitive.


## -parameters




### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>, <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>, <a href="https://msdn.microsoft.com/c8a590f2-3249-437f-a320-c7443d42b792">RegOpenKeyEx</a>, or 
 <b>RegOpenKeyTransacted</b> function. It can also be one of the following 
<a href="https://msdn.microsoft.com/db747656-b414-4594-ad39-6b476799060c">predefined keys</a>:

<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the registry subkey to be opened. 

Key names are not case sensitive.

If this parameter is <b>NULL</b> or a pointer to an empty string, the function will open a new handle to the key identified by the <i>hKey</i> parameter.

For more information, see 
<a href="https://msdn.microsoft.com/a6d3a884-f181-46a5-b655-226c68792e08">Registry Element Size Limits</a>.


### -param ulOptions [in]

This parameter is reserved and must be zero.


### -param samDesired [in]

A mask that specifies the desired access rights to the key. The function fails if the security descriptor of the key does not permit the requested access for the calling process. For more information, see 
<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>.


### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. If the key is not one of the predefined registry keys, call the 
<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a> function after you have finished using the handle.


### -param hTransaction [in]

A handle to an active transaction. This handle is returned by the <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


### -param pExtendedParemeter

TBD




#### - pExtendedParameter

This parameter is reserved and must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.




## -remarks



When a key is opened using this function, subsequent operations on the key are transacted. If a non-transacted operation is performed on the key before the transaction is committed, the transaction is rolled back. After a transaction is committed or rolled back, you must re-open the key using the <a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a> or <b>RegOpenKeyTransacted</b> function with an active transaction handle to make additional operations transacted. For more information about transactions, see <a href="fs.ktm_start_page">Kernel Transaction Manager</a>.

Note that subsequent operations on subkeys of this key are not automatically transacted. Therefore,  the <a href="https://msdn.microsoft.com/41fde6a5-647c-4293-92b8-74be54fa4136">RegDeleteKeyEx</a> function does not perform a transacted delete operation. Instead, use the <a href="https://msdn.microsoft.com/4c67e08b-4338-4441-8300-6b6ed31d4b21">RegDeleteKeyTransacted</a> function to perform a transacted delete operation.

Unlike the 
<a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a> function, the 
<b>RegOpenKeyTransacted</b> function does not create the specified key if the key does not exist in the registry.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="https://msdn.microsoft.com/10a8cbfb-52dc-436a-827e-78f12eb62af0">RegOpenCurrentUser</a> function.

A single registry key can be opened only 65,534 times. When attempting the 65,535<sup>th</sup> open operation, this function fails with ERROR_NO_SYSTEM_RESOURCES.




## -see-also




<a href="https://msdn.microsoft.com/10175499-abf3-4694-9594-bb97b43f3fa5">RegCloseKey</a>



<a href="https://msdn.microsoft.com/f18e5ff9-41c3-4c26-8d01-a8ec69bcdef2">RegCreateKeyTransacted</a>



<a href="https://msdn.microsoft.com/a2310ca0-1b9f-48d1-a3b5-ea3a528bfaba">RegDeleteKeyTransacted</a>



<a href="https://msdn.microsoft.com/a490b748-42e8-462b-9a7f-a8b21438ea79">Registry Functions</a>



<a href="https://msdn.microsoft.com/ffb06903-593e-47ce-adb2-baed5d379110">Registry Overview</a>
 

 

