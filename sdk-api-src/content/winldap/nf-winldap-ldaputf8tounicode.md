---
UID: NF:winldap.LdapUTF8ToUnicode
title: LdapUTF8ToUnicode function
author: windows-sdk-content
description: Used to translate strings for modules that do not have the UTF-8 code page.
old-location: ldap\ldaputf8tounicode.htm
old-project: LDAP
ms.assetid: 4c36ce90-8cc6-4dee-b990-5d283613ba11
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: LdapUTF8ToUnicode, LdapUTF8ToUnicode function [LDAP], _ldap_ldaputf8tounicode, ldap.ldaputf8tounicode, winldap/LdapUTF8ToUnicode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	LdapUTF8ToUnicode
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LdapUTF8ToUnicode function


## -description


The <b>LdapUTF8ToUnicode</b> function is used to translate strings for modules that do not have the UTF-8 code page.


## -parameters




### -param lpSrcStr [in]

A pointer to a null-terminated UTF-8 string to convert.


### -param cchSrc [in]

An integer that specifies the size, in characters, of the <i>lpSrcStr</i> string.


### -param lpDestStr [out]

A pointer to a buffer that receives the converted Unicode string, without a null terminator.


### -param cchDest [in]

An integer that specifies the size, in characters, of the <i>lpDestStr</i> buffer.


## -returns



The return value is the number of characters written to the <i>lpDestStr</i> buffer.
      If the <i>lpDestStr</i> buffer is too small, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_INSUFFICIENT_BUFFER</b>.

When the <i>cchDest</i> parameter is zero, the required size of the destination buffer is returned.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/9a56cf0e-ff6c-4b0a-9138-495d9cebfc99">LdapUnicodeToUTF8</a>
 

 

