---
UID: NF:winreg.RegOpenKeyTransactedA
title: RegOpenKeyTransactedA function (winreg.h)
description: Opens the specified registry key and associates it with a transaction. (ANSI)
helpviewer_keywords: ["RegOpenKeyTransactedA", "winreg/RegOpenKeyTransactedA"]
old-location: base\regopenkeytransacted.htm
tech.root: winprog
ms.assetid: 11663ed2-d17c-4f08-be7b-9b591271fbcd
ms.date: 12/05/2018
ms.keywords: RegOpenKeyTransacted, RegOpenKeyTransacted function, RegOpenKeyTransactedA, RegOpenKeyTransactedW, base.regopenkeytransacted, winreg/RegOpenKeyTransacted, winreg/RegOpenKeyTransactedA, winreg/RegOpenKeyTransactedW
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegOpenKeyTransactedA
 - winreg/RegOpenKeyTransactedA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-registry-l2-3-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-Registry-l2-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-Core-Registry-l2-2-0.dll
api_name:
 - RegOpenKeyTransacted
 - RegOpenKeyTransactedA
 - RegOpenKeyTransactedW
---

# RegOpenKeyTransactedA function


## -description

Opens the specified registry key and associates it with a  transaction. Note that key names are not case sensitive.

## -parameters

### -param hKey [in]

A handle to an open registry key. This handle is returned by the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>, <a href="/windows/desktop/api/winreg/nf-winreg-regopenkeyexa">RegOpenKeyEx</a>, or 
 <b>RegOpenKeyTransacted</b> function. It can also be one of the following 
<a href="/windows/desktop/SysInfo/predefined-keys">predefined keys</a>:

<b>HKEY_CLASSES_ROOT</b>
<b>HKEY_CURRENT_USER</b>
<b>HKEY_LOCAL_MACHINE</b>
<b>HKEY_USERS</b>

### -param lpSubKey [in, optional]

The name of the registry subkey to be opened. 

Key names are not case sensitive.

If the <i>lpSubKey</i> parameter is <b>NULL</b> or a pointer to an empty string,
and if <i>hKey</i> is a predefined key,
then the system refreshes the predefined key,
and <i>phkResult</i> receives the same <i>hKey</i> handle passed into the function.
Otherwise, <i>phkResult</i> receives a new handle to the opened key.

For more information, see 
<a href="/windows/desktop/SysInfo/registry-element-size-limits">Registry Element Size Limits</a>.

### -param ulOptions [in]

This parameter is reserved and must be zero.

### -param samDesired [in]

A mask that specifies the desired access rights to the key. The function fails if the security descriptor of the key does not permit the requested access for the calling process. For more information, see 
<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

### -param phkResult [out]

A pointer to a variable that receives a handle to the opened key. If the key is not one of the predefined registry keys, call the 
<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a> function after you have finished using the handle.

### -param hTransaction [in]

A handle to an active transaction. This handle is returned by the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

### -param pExtendedParemeter

This parameter is reserved and must be <b>NULL</b>.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is a nonzero error code defined in Winerror.h. You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function with the FORMAT_MESSAGE_FROM_SYSTEM flag to get a generic description of the error.

## -remarks

When a key is opened using this function, subsequent operations on the key are transacted. If a non-transacted operation is performed on the key before the transaction is committed, the transaction is rolled back. After a transaction is committed or rolled back, you must re-open the key using the <a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a> or <b>RegOpenKeyTransacted</b> function with an active transaction handle to make additional operations transacted. For more information about transactions, see <a href="/windows/desktop/Ktm/kernel-transaction-manager-portal">Kernel Transaction Manager</a>.

Note that subsequent operations on subkeys of this key are not automatically transacted. Therefore,  the <a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa">RegDeleteKeyEx</a> function does not perform a transacted delete operation. Instead, use the <a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeytransacteda">RegDeleteKeyTransacted</a> function to perform a transacted delete operation.

Unlike the 
<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a> function, the 
<b>RegOpenKeyTransacted</b> function does not create the specified key if the key does not exist in the registry.

If your service or application impersonates different users, do not use this function with <b>HKEY_CURRENT_USER</b>. Instead, call the <a href="/windows/desktop/api/winreg/nf-winreg-regopencurrentuser">RegOpenCurrentUser</a> function.

If the key returned in <i>phkResult</i> is a predefined registry key, it is not included in the provided transaction.

A single registry key can be opened only 65,534 times. When attempting the 65,535<sup>th</sup> open operation, this function fails with ERROR_NO_SYSTEM_RESOURCES.





> [!NOTE]
> The winreg.h header defines RegOpenKeyTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeytransacteda">RegCreateKeyTransacted</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regdeletekeya">RegDeleteKeyTransacted</a>



<a href="/windows/desktop/SysInfo/registry-functions">Registry Functions</a>



<a href="/windows/desktop/SysInfo/registry">Registry Overview</a>
