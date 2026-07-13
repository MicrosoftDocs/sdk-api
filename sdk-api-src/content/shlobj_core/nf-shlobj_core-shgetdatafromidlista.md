---
UID: NF:shlobj_core.SHGetDataFromIDListA
title: SHGetDataFromIDListA function (shlobj_core.h)
description: Retrieves extended property data from a relative identifier list. (ANSI)
helpviewer_keywords: ["SHGDFIL_DESCRIPTIONID", "SHGDFIL_FINDDATA", "SHGDFIL_NETRESOURCE", "SHGetDataFromIDListA", "shlobj_core/SHGetDataFromIDListA"]
old-location: shell\SHGetDataFromIDList.htm
tech.root: shell
ms.assetid: 11c041bd-22fd-46a4-b75c-cc86ee771241
ms.date: 12/05/2018
ms.keywords: SHGDFIL_DESCRIPTIONID, SHGDFIL_FINDDATA, SHGDFIL_NETRESOURCE, SHGetDataFromIDList, SHGetDataFromIDList function [Windows Shell], SHGetDataFromIDListA, SHGetDataFromIDListW, _win32_SHGetDataFromIDList, shell.SHGetDataFromIDList, shlobj_core/SHGetDataFromIDList, shlobj_core/SHGetDataFromIDListA, shlobj_core/SHGetDataFromIDListW
req.header: shlobj_core.h
req.include-header: Shlobj.h, Shlobj_core.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetDataFromIDListW (Unicode) and SHGetDataFromIDListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetDataFromIDListA
 - shlobj_core/SHGetDataFromIDListA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHGetDataFromIDList
 - SHGetDataFromIDListA
 - SHGetDataFromIDListW
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHGetDataFromIDListA function


## -description

Retrieves extended property data from a relative identifier list.

## -parameters

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

The address of the parent <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface. This must be the immediate parent of the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure referenced by the <i>pidl</i> parameter.

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure that identifies the object relative to the folder specified in <i>psf</i>.

### -param nFormat

Type: <b>int</b>

The format in which the data is being requested. This parameter must be set to one of the following values.



#### SHGDFIL_FINDDATA

Format used for file system objects. The <i>pv</i> parameter is the address of a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure.



#### SHGDFIL_NETRESOURCE

Format used for network resources. The <i>pv</i> parameter is the address of a <a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structure.



#### SHGDFIL_DESCRIPTIONID


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 4.71</a>. Format used for network resources. The <i>pv</i> parameter is the address of an <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid">SHDESCRIPTIONID</a> structure.

### -param pv [out]

Type: <b>void*</b>

A pointer to a buffer that, when this function returns successfully, receives the requested data. The format of this buffer is determined by <i>nFormat</i>.

If <i>nFormat</i> is <b>SHGDFIL_NETRESOURCE</b>, there are two possible cases. If the buffer is large enough, the net resource's string information (fields for the network name, local name, provider, and comments) will be placed into the buffer. If the buffer is not large enough, only the net resource structure will be placed into the buffer and the string information pointers will be <b>NULL</b>.

### -param cb

Type: <b>int</b>

Size of the buffer at <i>pv</i>, in bytes.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or E_INVALIDARG otherwise.

## -remarks

This function extracts only information that is present in the pointer to an item identifier list (PIDL). Since the content of a PIDL depends on the folder object that created the PIDL, there is no guarantee that all requested information will be available. In addition, the information that is returned reflects the state of the object at the time the PIDL was created. The current state of the object could be different. For example, if you set <i>nFormat</i> to <b>SHGDFIL_FINDDATA</b>, the function might assign meaningful values to only some of the members of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure. The remaining members will be set to zero. To retrieve complete current information on a file system file or folder, use standard file system functions such as <a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletime">GetFileTime</a> or <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>.

E_INVALIDARG is returned if the <i>psf</i>, <i>pidl</i>, <i>pv</i>, or <i>cb</i> parameter does not match the <i>nFormat</i> parameter, or if <i>nFormat</i> is not one of the specific SHGDFIL_ values shown above.




> [!NOTE]
> The shlobj_core.h header defines SHGetDataFromIDList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
