---
UID: NF:winbase.GetPrivateProfileStructW
title: GetPrivateProfileStructW function (winbase.h)
description: The GetPrivateProfileStructW (Unicode) function (winbase.h) retrieves the data associated with a key in the specified section of an initialization file.
helpviewer_keywords: ["GetPrivateProfileStruct", "GetPrivateProfileStruct function", "GetPrivateProfileStructW", "_win32_getprivateprofilestruct", "base.getprivateprofilestruct", "winbase/GetPrivateProfileStruct", "winbase/GetPrivateProfileStructW"]
old-location: base\getprivateprofilestruct.htm
tech.root: winprog
ms.assetid: a14ba43e-d16d-4c52-a8ac-0d4c71229b7b
ms.date: 08/04/2022
ms.keywords: GetPrivateProfileStruct, GetPrivateProfileStruct function, GetPrivateProfileStructA, GetPrivateProfileStructW, _win32_getprivateprofilestruct, base.getprivateprofilestruct, winbase/GetPrivateProfileStruct, winbase/GetPrivateProfileStructA, winbase/GetPrivateProfileStructW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetPrivateProfileStructW (Unicode) and GetPrivateProfileStructA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPrivateProfileStructW
 - winbase/GetPrivateProfileStructW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetPrivateProfileStruct
 - GetPrivateProfileStructA
 - GetPrivateProfileStructW
---

# GetPrivateProfileStructW function


## -description

Retrieves the data associated with a key in the specified section of an initialization file. As it retrieves the data, the function calculates a checksum and compares it with the checksum calculated by the 
<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilestructa">WritePrivateProfileStruct</a> function when the data was added to the file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows-based applications. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpszSection [in]

The name of the section in the initialization file.

### -param lpszKey [in]

The name of the key whose data is to be retrieved.

### -param lpStruct [out]

A pointer to the buffer that receives the data associated with the file, section, and key names.

### -param uSizeStruct [in]

The size of the buffer pointed to by the <i>lpStruct</i> parameter, in bytes.

### -param szFile [in]

The name of the initialization file. If this parameter does not contain a full path to the file, the system searches for the file in the Windows directory.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

A section in the initialization file must have the following form:
				
			


``` syntax
[section]
key=data
      .
      .
      .
```

The system maps most .ini file references to the registry, using the mapping defined under the following registry key:<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows NT</b>&#92;<b>CurrentVersion</b>&#92;<b>IniFileMapping</b>



This mapping is likely if an application modifies system-component initialization files, such as Control.ini, System.ini, and Winfile.ini. In these cases, the 
 function retrieves information from the registry, not from the initialization file; the change in the storage location has no effect on the function's behavior.

The profile functions use the following steps to locate initialization information:

<ol>
<li>Look in the registry for the name of the initialization file, say MyFile.ini, under <b>IniFileMapping</b>.</li>
<li>Look for the section name specified by <i>lpAppName</i>. This will be a named value under <b>myfile.ini</b>, or a subkey of <b>myfile.ini</b>, or will not exist.</li>
<li>If the section name specified by <i>lpAppName</i> is a named value under <b>myfile.ini</b>, then that value specifies where in the registry you will find the keys for the section.</li>
<li>If the section name specified by <i>lpAppName</i> is a subkey of <b>myfile.ini</b>, then named values under that subkey specify where in the registry you will find the keys for the section. If the key you are looking for does not exist as a named value, then there will be an unnamed value (shown as <b>&lt;No Name&gt;</b>) that specifies the default location in the registry where you will find the key.</li>
<li>If the section name specified by <i>lpAppName</i> does not exist as a named value or as a subkey under <b>myfile.ini</b>, then there will be an unnamed value (shown as <b>&lt;No Name&gt;</b>) under <b>myfile.ini</b> that specifies the default location in the registry where you will find the keys for the section.</li>
<li>If there is no <b>myfile.ini</b> subkey, or if it does not contain an entry for the section name, then look for the actual MyFile.ini on the disk and read its contents.</li>
</ol>
When looking at values in the registry that specify other registry locations, there are several prefixes that change the behavior of the .ini file mapping:

<ul>
<li>! - this character forces all writes to go both to the registry and to the .ini file on disk.</li>
<li># - this character causes the registry value to be set to the value in the Windows 3.1 .ini file when a new user logs in for the first time after setup.</li>
<li>@ - this character prevents any reads from going to the .ini file on disk if the requested data is not found in the registry.</li>
<li>USR: - this prefix stands for <b>HKEY_CURRENT_USER</b>, and the text after the prefix is relative to that key.</li>
<li>SYS: - this prefix stands for <b>HKEY_LOCAL_MACHINE\SOFTWARE</b>, and the text after the prefix is relative to that key.</li>
</ul>




> [!NOTE]
> The winbase.h header defines GetPrivateProfileStruct as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilestructa">WritePrivateProfileStruct</a>
