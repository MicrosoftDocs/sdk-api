---
UID: NE:shlwapi.__unnamed_enum_0
title: "__unnamed_enum_0"
author: windows-sdk-content
description: Provides information to the IQueryAssociations interface methods.
old-location: shell\ASSOCF_str.htm
tech.root: shell
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ASSOCF, ASSOCF enumeration [Windows Shell], ASSOCF_IGNOREBASECLASS, ASSOCF_INIT_BYEXENAME, ASSOCF_INIT_DEFAULTTOFOLDER, ASSOCF_INIT_DEFAULTTOSTAR, ASSOCF_INIT_FIXED_PROGID, ASSOCF_INIT_FOR_FILE, ASSOCF_INIT_IGNOREUNKNOWN, ASSOCF_INIT_NOREMAPCLSID, ASSOCF_IS_PROTOCOL, ASSOCF_NOFIXUPS, ASSOCF_NONE, ASSOCF_NOTRUNCATE, ASSOCF_NOUSERSETTINGS, ASSOCF_OPEN_BYEXENAME, ASSOCF_REMAPRUNDLL, ASSOCF_VERIFY, __unnamed_enum_0, _win32_ASSOCF_str, shell.ASSOCF_str, shlwapi/ASSOCF, shlwapi/ASSOCF_IGNOREBASECLASS, shlwapi/ASSOCF_INIT_BYEXENAME, shlwapi/ASSOCF_INIT_DEFAULTTOFOLDER, shlwapi/ASSOCF_INIT_DEFAULTTOSTAR, shlwapi/ASSOCF_INIT_FIXED_PROGID, shlwapi/ASSOCF_INIT_FOR_FILE, shlwapi/ASSOCF_INIT_IGNOREUNKNOWN, shlwapi/ASSOCF_INIT_NOREMAPCLSID, shlwapi/ASSOCF_IS_PROTOCOL, shlwapi/ASSOCF_NOFIXUPS, shlwapi/ASSOCF_NONE, shlwapi/ASSOCF_NOTRUNCATE, shlwapi/ASSOCF_NOUSERSETTINGS, shlwapi/ASSOCF_OPEN_BYEXENAME, shlwapi/ASSOCF_REMAPRUNDLL, shlwapi/ASSOCF_VERIFY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlwapi.h
api_name:
 - ASSOCF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# __unnamed_enum_0 enumeration


## -description


Provides information to the <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface methods.


## -enum-fields




### -field ASSOCF_NONE

None of the following options are set.


### -field ASSOCF_INIT_NOREMAPCLSID

Instructs <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface methods not to map CLSID values to ProgID values.


### -field ASSOCF_INIT_BYEXENAME

Identifies the value of the <i>pwszAssoc</i> parameter of <a href="https://msdn.microsoft.com/cb1bcfc1-dbaa-48f8-8547-408f6560753e">IQueryAssociations::Init</a> as an executable file name. If this flag is not set, the root key will be set to the ProgID associated with the <b>.exe</b> key instead of the executable file's ProgID.


### -field ASSOCF_OPEN_BYEXENAME

Identical to <a href="https://msdn.microsoft.com/e67d0282-9090-43e6-aedf-bb1fc0443221">ASSOCF_INIT_BYEXENAME</a>.


### -field ASSOCF_INIT_DEFAULTTOSTAR

Specifies that when an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the <b>*</b> subkey.


### -field ASSOCF_INIT_DEFAULTTOFOLDER

Specifies that when a <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the <b>Folder</b> subkey.


### -field ASSOCF_NOUSERSETTINGS

Specifies that only <b>HKEY_CLASSES_ROOT</b> should be searched, and that <b>HKEY_CURRENT_USER</b> should be ignored.


### -field ASSOCF_NOTRUNCATE

Specifies that the return string should not be truncated. Instead, return an error value and the required size for the complete string.


### -field ASSOCF_VERIFY

Instructs <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> methods to verify that data is accurate. This setting allows <b>IQueryAssociations</b> methods to read data from the user's hard disk for verification. For example, they can check the friendly name in the registry against the one stored in the .exe file. Setting this flag typically reduces the efficiency of the method.


### -field ASSOCF_REMAPRUNDLL

Instructs <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> methods to ignore Rundll.exe and return information about its target. Typically <b>IQueryAssociations</b> methods return information about the first .exe or .dll in a command string. If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.


### -field ASSOCF_NOFIXUPS

Instructs <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.


### -field ASSOCF_IGNOREBASECLASS

Specifies that the BaseClass value should be ignored.


### -field ASSOCF_INIT_IGNOREUNKNOWN

<b>Introduced in Windows 7</b>. Specifies that the "Unknown" ProgID should be ignored; instead, fail.


### -field ASSOCF_INIT_FIXED_PROGID

<b>Introduced in Windows 8</b>. Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.


### -field ASSOCF_IS_PROTOCOL

<b>Introduced in Windows 8</b>. Specifies that the value is a protocol, and should be mapped using the current user defaults.


### -field ASSOCF_INIT_FOR_FILE

<b>Introduced in Windows 8.1</b>. Specifies that the ProgID corresponds with a file extension based association. Use together with <b>ASSOCF_INIT_FIXED_PROGID</b>.


### -field ASSOCF_IS_FULL_URI


### -field ASSOCF_PER_MACHINE_ONLY


### -field ASSOCF_APP_TO_APP




## -see-also




<a href="https://msdn.microsoft.com/9eaeb885-0428-48c3-82a7-5dc21d5015ce">AssocQueryKey</a>



<a href="https://msdn.microsoft.com/026b841d-b831-475e-a788-2c79801e20b8">AssocQueryString</a>



<a href="https://msdn.microsoft.com/6816f7fe-9a70-4c5f-bd45-d1ca96d4ebd0">AssocQueryStringByKey</a>
 

 

