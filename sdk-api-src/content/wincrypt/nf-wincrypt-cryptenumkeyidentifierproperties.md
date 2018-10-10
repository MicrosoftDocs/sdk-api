---
UID: NF:wincrypt.CryptEnumKeyIdentifierProperties
title: CryptEnumKeyIdentifierProperties function
author: windows-sdk-content
description: The CryptEnumKeyIdentifierProperties function enumerates key identifiers and their properties.
old-location: security\cryptenumkeyidentifierproperties.htm
tech.root: seccrypto
ms.assetid: 6e57d935-4cfb-44af-b1c6-6c399c959452
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CryptEnumKeyIdentifierProperties, CryptEnumKeyIdentifierProperties function [Security], _crypto2_cryptenumkeyidentifierproperties, security.cryptenumkeyidentifierproperties, wincrypt/CryptEnumKeyIdentifierProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptEnumKeyIdentifierProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptEnumKeyIdentifierProperties function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptEnumKeyIdentifierProperties</b> function enumerates key identifiers and their properties. This function is not called in a loop. Rather, it loops internally until the last key identifier property is enumerated or the callback function returns <b>FALSE</b>. If <i>dwPropId</i> is zero or if the properties of the key identifier match the <i>dwPropId</i>, the callback function is called.


## -parameters




### -param pKeyIdentifier [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure that contains the key identifier. 




If <i>pKeyIdentifier</i> is <b>NULL</b>, the function enumerates all key identifiers.

If <i>pKeyIdentifier</i> is not <b>NULL</b>, the callback function <i>pfnEnum</i> is only called for the specified key identifier.


### -param dwPropId [in]

Indicates the property identifier to be listed. 




If <i>dwPropId</i> is set to zero, this function calls the callback function with all the properties.

If <i>dwPropId</i> is not zero and <i>pKeyIdentifier</i> is <b>NULL</b>, the callback function is called only for those key identifiers that have the specified property (sets the <i>cProp</i> parameter of <i>pfnEnum</i> to one). All key identifiers that do not have the property are skipped.

Any certificate property identifier can be used.


### -param dwFlags [in]

By default, the list of key identifiers for the CurrentUser is searched. If CRYPT_KEYID_MACHINE_FLAG is set, the list of key identifiers of the LocalMachine (if <i>pwszComputerName</i> is <b>NULL</b>) or of a remote computer (if <i>pwszComputerName</i> is not <b>NULL</b>) is searched. For more information, see <i>pwszComputerName</i>.


### -param pwszComputerName [in, optional]

A pointer to the name of a remote computer to be searched. If CRYPT_KEYID_MACHINE_FLAG is set in <i>dwFlags</i>, the remote computer is searched for a list of key identifiers. If the local computer is to be searched and not a remote computer, <i>pwszComputerName</i> is set to <b>NULL</b>.


### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.


### -param pvArg [in, optional]

A pointer to data to be passed to the callback function. The type is a void that allows the application to declare, define, and initialize a structure or argument to hold any information.


### -param pfnEnum [in]

A pointer to an application-defined callback function that is executed for each key identifier entry that matches the input parameters. For details about the callback functions parameters, see <a href="https://msdn.microsoft.com/c4461b79-d216-4d4a-bd5d-9260ec897c14">CRYPT_ENUM_KEYID_PROP</a>.


## -returns



The <b>CryptEnumKeyIdentifierProperties</b> function repeatedly calls the <a href="https://msdn.microsoft.com/c4461b79-d216-4d4a-bd5d-9260ec897c14">CRYPT_ENUM_KEYID_PROP</a> callback function until the last key identifier is enumerated or the callback function returns <b>FALSE</b>.

If the main function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

To continue enumeration, the function returns <b>TRUE</b>.

To stop enumeration, the function returns <b>FALSE</b> and sets the last error code.




## -remarks



A key identifier can have the same properties as a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>.


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/5ca160fd-8a63-46fa-99ce-e01a6acb81f4">Example C Program: Working with Key Identifiers</a>.

<div class="code"></div>



## -see-also




<a href="cryptography_functions.htm">Base Cryptography Functions</a>



<a href="https://msdn.microsoft.com/bc0511c1-0699-4959-afd7-a838c91c77d5">CryptGetKeyIdentifierProperty</a>



<a href="https://msdn.microsoft.com/0970aaaa-3f9a-4471-bd21-5de8746f94a2">CryptSetKeyIdentifierProperty</a>
 

 

