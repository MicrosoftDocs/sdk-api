---
UID: NS:winnls._FILEMUIINFO
title: FILEMUIINFO (winnls.h)
description: Contains information about a file, related to its use with MUI.
helpviewer_keywords: ["*PFILEMUIINFO","FILEMUIINFO","FILEMUIINFO structure [Internationalization for Windows Applications]","PFILEMUIINFO","PFILEMUIINFO structure pointer [Internationalization for Windows Applications]","_win32_FILEMUIINFO","intl.filemuiinfo","winnls/FILEMUIINFO","winnls/PFILEMUIINFO"]
old-location: intl\filemuiinfo.htm
tech.root: Intl
ms.assetid: 4c757d19-ac66-4ba4-a691-f575f61961be
ms.date: 12/05/2018
ms.keywords: '*PFILEMUIINFO, FILEMUIINFO, FILEMUIINFO structure [Internationalization for Windows Applications], PFILEMUIINFO, PFILEMUIINFO structure pointer [Internationalization for Windows Applications], _win32_FILEMUIINFO, intl.filemuiinfo, winnls/FILEMUIINFO, winnls/PFILEMUIINFO'
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: FILEMUIINFO, *PFILEMUIINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILEMUIINFO
 - winnls/_FILEMUIINFO
 - PFILEMUIINFO
 - winnls/PFILEMUIINFO
 - FILEMUIINFO
 - winnls/FILEMUIINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - FILEMUIINFO
---

# FILEMUIINFO structure


## -description

Contains information about a file, related to its use with MUI. Most of this data is stored in the resource configuration data for the particular file. When this structure is retrieved by <a href="/windows/desktop/api/winnls/nf-winnls-getfilemuiinfo">GetFileMUIInfo</a>, not all fields are necessarily filled in. The fields used depend on the flags that the application has passed to that function.


<div class="alert"><b>Note</b>  Your MUI applications can use the MUI macros to access this structure.</div>
<div> </div>

## -struct-fields

### -field dwSize

Size of the structure, including the buffer, which can be extended past the 8 bytes declared. The minimum value allowed is <code>sizeof(FILEMUIINFO)</code>.

### -field dwVersion

Version of the structure. The current version is 0x001.

### -field dwFileType

The file type. Possible values are:

<ul>
<li>MUI_FILETYPE_NOT_LANGUAGE_NEUTRAL. The input file does not have resource configuration data. This file type is typical for older executable files. If this file type is specified, the other file types will not provide useful information.</li>
<li>MUI_FILETYPE_LANGUAGE_NEUTRAL_MAIN. The input file is an LN file.</li>
<li>MUI_FILETYPE_LANGUAGE_NEUTRAL_MUI. The input file is a language-specific resource file.</li>
</ul>

### -field pChecksum

Pointer to a 128-bit checksum for the file, if it is either an LN file or a language-specific resource file.

### -field pServiceChecksum

Pointer to a 128-bit checksum for the file, used for servicing.

### -field dwLanguageNameOffset

Offset, in bytes, from the beginning of the structure to the language name string for a language-specific resource file, or to the ultimate fallback language name string for an LN file.

### -field dwTypeIDMainSize

Size of the array for which the offset is indicated by <i>dwTypeIDMainOffset</i>. The size also corresponds to the number of strings in the multi-string array indicated by <i>dwTypeNameMainOffset</i>.

### -field dwTypeIDMainOffset

Offset, in bytes, from the beginning of the structure to a DWORD array enumerating the resource types contained in the LN file.

### -field dwTypeNameMainOffset

Offset, in bytes, from the beginning of the structure to a series of null-terminated strings in a multi-string array enumerating the resource names contained in the LN file.

### -field dwTypeIDMUISize

Size of the array with the offset indicated by <i>dwTypeIDMUIOffset</i>. The size also corresponds to the number of strings in the series of strings indicated by <i>dwTypeNameMUIOffset</i>.

### -field dwTypeIDMUIOffset

Offset, in bytes, from the beginning of the structure to a DWORD array enumerating the resource types contained in the LN file.

### -field dwTypeNameMUIOffset

Offset, in bytes, from the beginning of the structure to a multi-string array enumerating the resource names contained in the LN file.

### -field abBuffer

Remainder of the allocated memory for this structure. See the Remarks section for correct use of this array.

## -remarks

All offsets are from the base of the structure. An offset of 0 indicates that the data is not available.

The following is an example showing how to access data for the position in the structure that is described by an offset. This example accesses the language name string with the position defined by <i>dwLanguageNameOffset</i>.


```cpp
PFILEMUIINFO pFileMUIInfo = NULL;

Allocate_pFileMUIInfo_AndPassTo_GetFileMUIInfo(&pFileMUIInfo);

LPWSTR lpszLang = reinterpret_cast<LPWSTR>(reinterpret_cast<BYTE*>(pFileMUIInfo) + pFileMUIInfo->dwLanguageNameOffset);

```


This example uses two reinterpret casts. First the code casts to BYTE* so the pointer arithmetic for the offset will be done in bytes. Then the code casts the resulting pointer to the desired type.

Alternatively, the code can be written as shown below. The effect is the same; the choice is strictly one of style.


```cpp
PFILEMUIINFO pFileMUIInfo = NULL;

Allocate_pFileMUIInfo_AndPassTo_GetFileMUIInfo(&pFileMUIInfo);

DWORD ix = pFileMUIInfo->dwLanguageNameOffset - offsetof(struct _FILEMUIINFO, abBuffer);
LPWSTR lpszLang = reinterpret_cast<LPWSTR>(&(pFileMUIInfo->abBuffer[ix]));

```


<h3><a id="C__Signature"></a><a id="c__signature"></a><a id="C__SIGNATURE"></a>C# Signature</h3>

```cpp
unsafe public struct FILEMUIINFO
        {
            public System.UInt32 dwSize;
            public System.UInt32 dwVersion;
            public System.UInt32 dwFileType;
            public fixed System.Byte pChecksum[16];
            public fixed System.Byte pServiceChecksum[16];
            public System.UInt32 dwLanguageNameOffset;
            public System.UInt32 dwTypeIDMainSize;
            public System.UInt32 dwTypeIDMainOffset;
            public System.UInt32 dwTypeNameMainOffset;
            public System.UInt32 dwTypeIDMUISize;
            public System.UInt32 dwTypeIDMUIOffset;
            public System.UInt32 dwTypeNameMUIOffset;
            public fixed System.Byte abBuffer[8];
        }

```

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getfilemuiinfo">GetFileMUIInfo</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-macros">Multilingual User Interface Macros</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-structures">Multilingual User Interface Structures</a>