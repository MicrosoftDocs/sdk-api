---
UID: NF:shlwapi.StrRetToBSTR
title: StrRetToBSTR function (shlwapi.h)
description: Accepts a STRRET structure returned by IShellFolder::GetDisplayNameOf that contains or points to a string, and returns that string as a BSTR.helpviewer_keywords: ["StrRetToBSTR","StrRetToBSTR function [Windows Shell]","_shell_StrRetToBSTR","shell.StrRetToBSTR","shlwapi/StrRetToBSTR"]
old-location: shell\StrRetToBSTR.htm
tech.root: shell
ms.assetid: 2a5a9a2b-74df-4521-a5b2-8fc91c3559eb
ms.date: 12/05/2018
ms.keywords: StrRetToBSTR, StrRetToBSTR function [Windows Shell], _shell_StrRetToBSTR, shell.StrRetToBSTR, shlwapi/StrRetToBSTR
f1_keywords:
- shlwapi/StrRetToBSTR
dev_langs:
- c++
req.header: shlwapi.h
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
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.5 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shlwapi.dll
api_name:
- StrRetToBSTR
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StrRetToBSTR function


## -description


Accepts a <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure returned by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a> that contains or points to a string, and returns that string as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a>.


## -parameters




### -param pstr [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure. When the function returns, this pointer is longer valid.


### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> that uniquely identifies a file object or subfolder relative to the parent folder. This value can be <b>NULL</b>.


### -param pbstr [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a>*</b>

A pointer to a variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> that receives the converted string.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>uType</i> member of the <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure pointed to by <i>pstr</i> is set to <b>STRRET_WSTR</b>, the <i>pOleStr</i> member of that structure is freed on return.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof">IShellFolder::GetDisplayNameOf</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-strrettobufa">StrRetToBuf</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-strrettostra">StrRetToStr</a>
 

 

