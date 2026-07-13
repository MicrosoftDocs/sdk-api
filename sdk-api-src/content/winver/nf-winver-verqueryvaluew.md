---
UID: NF:winver.VerQueryValueW
title: VerQueryValueW function (winver.h)
description: Retrieves specified version information from the specified version-information resource. (Unicode)
helpviewer_keywords: ["VerQueryValue", "VerQueryValue function [Menus and Other Resources]", "VerQueryValueW", "_win32_VerQueryValue", "_win32_verqueryvalue_cpp", "menurc.verqueryvalue", "winui._win32_verqueryvalue", "winver/VerQueryValue", "winver/VerQueryValueW"]
old-location: menurc\verqueryvalue.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\versioninformation\versioninformationreference\versioninformationfunctions\verqueryvalue.htm
ms.date: 12/05/2018
ms.keywords: VerQueryValue, VerQueryValue function [Menus and Other Resources], VerQueryValueA, VerQueryValueW, _win32_VerQueryValue, _win32_verqueryvalue_cpp, menurc.verqueryvalue, winui._win32_verqueryvalue, winver/VerQueryValue, winver/VerQueryValueA, winver/VerQueryValueW
req.header: winver.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VerQueryValueW (Unicode) and VerQueryValueA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Version.lib
req.dll: Api-ms-win-core-version-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VerQueryValueW
 - winver/VerQueryValueW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-version-l1-1-0.dll
 - API-MS-Win-Core-version-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-versionansi-l1-1-0.dll
 - API-MS-Win-DownLevel-version-l1-1-0.dll
 - API-MS-Win-Core-Versionansi-L1-1-1.dll
 - API-MS-Win-Core-Version-L1-1-1.dll
 - version.dll
api_name:
 - VerQueryValue
 - VerQueryValueA
 - VerQueryValueW
---

# VerQueryValueW function


## -description

Retrieves specified version information from the specified version-information resource. To retrieve the appropriate resource, before you call <b>VerQueryValue</b>, you must first call the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a> function, and then the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a> function.

## -parameters

### -param pBlock [in]

Type: <b>LPCVOID</b>

The version-information resource returned by the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a> function.

### -param lpSubBlock [in]

Type: <b>LPCTSTR</b>

The version-information value to be retrieved. The string must consist of names separated by backslashes (\\) and it must have one of the following forms. 





#### \

The root block. The function retrieves a pointer to the <a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure for the version-information resource.



#### \VarFileInfo\Translation

The translation array in a <a href="/windows/desktop/menurc/var-str">Var</a> variable information structure—the <b>Value</b> member of this structure. The function retrieves a pointer to this array of language and code page identifiers. An application can use these identifiers to access a language-specific <a href="/windows/desktop/menurc/stringtable">StringTable</a> structure (using the <b>szKey</b> member) in the version-information resource.



#### \StringFileInfo\lang-codepage\string-name

A value in a language-specific <a href="/windows/desktop/menurc/stringtable">StringTable</a> structure. The <i>lang-codepage</i> name is a concatenation of a language and code page identifier pair found as a <b>DWORD</b> in the translation array for the resource. Here the <i>lang-codepage</i> name must be specified as a hexadecimal string. The <i>string-name</i> name must be one of the predefined strings described in the following Remarks section. The function retrieves a string value specific to the language and code page indicated.

### -param lplpBuffer [out]

Type: <b>LPVOID*</b>

When this method returns, contains the address of a pointer to the requested version information in the buffer pointed to by <i>pBlock</i>. The memory pointed to by <i>lplpBuffer</i> is freed when the associated <i>pBlock</i> memory is freed.

### -param puLen [out]

Type: <b>PUINT</b>

When this method returns, contains a pointer to the size of the requested data pointed to by <i>lplpBuffer</i>: for version information values, the length in characters of the string stored at <i>lplpBuffer</i>; for translation array values, the size in bytes of the array stored at <i>lplpBuffer</i>; and for root block, the size in bytes of the structure.


##### - lpSubBlock.\

The root block. The function retrieves a pointer to the <a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure for the version-information resource.


##### - lpSubBlock.\StringFileInfo\lang-codepage\string-name

A value in a language-specific <a href="/windows/desktop/menurc/stringtable">StringTable</a> structure. The <i>lang-codepage</i> name is a concatenation of a language and code page identifier pair found as a <b>DWORD</b> in the translation array for the resource. Here the <i>lang-codepage</i> name must be specified as a hexadecimal string. The <i>string-name</i> name must be one of the predefined strings described in the following Remarks section. The function retrieves a string value specific to the language and code page indicated. 


##### - lpSubBlock.\VarFileInfo\Translation

The translation array in a <a href="/windows/desktop/menurc/var-str">Var</a> variable information structure—the <b>Value</b> member of this structure. The function retrieves a pointer to this array of language and code page identifiers. An application can use these identifiers to access a language-specific <a href="/windows/desktop/menurc/stringtable">StringTable</a> structure (using the <b>szKey</b> member) in the version-information resource.

## -returns

Type: <b>BOOL</b>

If the specified version-information structure exists, and version information is available, the return value is nonzero. If the address of the length buffer is zero, no value is available for the specified version-information name.

If the specified name does not exist or the specified resource is not valid, the return value is zero.

## -remarks

 This function works on 16-, 32-, and 64-bit file images.

The following are predefined version information Unicode strings.

<table class="clsStd">
<tr>
<td>Comments</td>
<td>InternalName</td>
<td>ProductName</td>
</tr>
<tr>
<td>CompanyName</td>
<td>LegalCopyright</td>
<td>ProductVersion</td>
</tr>
<tr>
<td>FileDescription</td>
<td>LegalTrademarks</td>
<td>PrivateBuild</td>
</tr>
<tr>
<td>FileVersion</td>
<td>OriginalFilename</td>
<td>SpecialBuild</td>
</tr>
</table>
 


#### Examples

The following example shows how to enumerate the available version languages and retrieve the FileDescription string-value for each language.

Be sure to call the <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a> and <a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a> functions before calling <b>VerQueryValue</b> to properly initialize the <i>pBlock</i> buffer.


```cpp
// Structure used to store enumerated languages and code pages.

HRESULT hr;

struct LANGANDCODEPAGE {
  WORD wLanguage;
  WORD wCodePage;
} *lpTranslate;

// Read the list of languages and code pages.

VerQueryValue(pBlock, 
              TEXT("\\VarFileInfo\\Translation"),
              (LPVOID*)&lpTranslate,
              &cbTranslate);

// Read the file description for each language and code page.

for( i=0; i < (cbTranslate/sizeof(struct LANGANDCODEPAGE)); i++ )
{
  hr = StringCchPrintf(SubBlock, 50,
            TEXT("\\StringFileInfo\\%04x%04x\\FileDescription"),
            lpTranslate[i].wLanguage,
            lpTranslate[i].wCodePage);
	if (FAILED(hr))
	{
	// TODO: write error handler.
	}

  // Retrieve file description for language and code page "i". 
  VerQueryValue(pBlock, 
                SubBlock, 
                &lpBuffer, 
                &dwBytes); 
}
```






> [!NOTE]
> The winver.h header defines VerQueryValue as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfoa">GetFileVersionInfo</a>



<a href="/windows/desktop/api/winver/nf-winver-getfileversioninfosizea">GetFileVersionInfoSize</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/string-str">String</a>



<a href="/windows/desktop/menurc/stringfileinfo">StringFileInfo</a>



<a href="/windows/desktop/menurc/stringtable">StringTable</a>



<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a>



<a href="/windows/desktop/menurc/vs-versioninfo">VS_VERSIONINFO</a>



<a href="/windows/desktop/menurc/var-str">Var</a>



<a href="/windows/desktop/menurc/varfileinfo">VarFileInfo</a>



<a href="/windows/desktop/menurc/version-information">Version Information</a>
