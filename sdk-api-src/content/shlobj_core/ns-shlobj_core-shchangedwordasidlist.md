---
UID: NS:shlobj_core._SHChangeDWORDAsIDList
title: SHChangeDWORDAsIDList (shlobj_core.h)
description: SHChangeDWORDAsIDList may be altered or unavailable.
helpviewer_keywords: ["*LPSHChangeDWORDAsIDList","LPSHChangeDWORDAsIDList","LPSHChangeDWORDAsIDList structure pointer [Windows Shell]","SHChangeDWORDAsIDList","SHChangeDWORDAsIDList structure [Windows Shell]","_SHChangeDWORDAsIDList","_shell_SHChangeDWORDAsIDList","shell.SHChangeDWORDAsIDList","shlobj_core/LPSHChangeDWORDAsIDList","shlobj_core/SHChangeDWORDAsIDList"]
old-location: shell\SHChangeDWORDAsIDList.htm
tech.root: shell
ms.assetid: ebc05a9c-ed2b-41ff-93fb-9d8059fa360c
ms.date: 12/05/2018
ms.keywords: '*LPSHChangeDWORDAsIDList, LPSHChangeDWORDAsIDList, LPSHChangeDWORDAsIDList structure pointer [Windows Shell], SHChangeDWORDAsIDList, SHChangeDWORDAsIDList structure [Windows Shell], _SHChangeDWORDAsIDList, _shell_SHChangeDWORDAsIDList, shell.SHChangeDWORDAsIDList, shlobj_core/LPSHChangeDWORDAsIDList, shlobj_core/SHChangeDWORDAsIDList'
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHChangeDWORDAsIDList, *LPSHChangeDWORDAsIDList
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHChangeDWORDAsIDList
 - shlobj_core/_SHChangeDWORDAsIDList
 - LPSHChangeDWORDAsIDList
 - shlobj_core/LPSHChangeDWORDAsIDList
 - SHChangeDWORDAsIDList
 - shlobj_core/SHChangeDWORDAsIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHChangeDWORDAsIDList
---

# SHChangeDWORDAsIDList structure


## -description

<p class="CCE_Message">[<b>SHChangeDWORDAsIDList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Stores two <b>DWORD</b> values in a form mimicking an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> so that they can be used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a>.

## -struct-fields

### -field cb

Type: <b>USHORT</b>

The size of the structure, in bytes.

### -field dwItem1

Type: <b>DWORD</b>

First <b>DWORD</b> value.

### -field dwItem2

Type: <b>DWORD</b>

Second <b>DWORD</b> value.

### -field cbZero

Type: <b>USHORT</b>

## -remarks

This example demonstrates the use of <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangeupdateimageidlist">SHChangeUpdateImageIDList</a> and <b>SHChangeDWORDAsIDList</b> by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a> to mimic the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea">SHUpdateImage</a> function.

                


```
void MyUpdateImage(LPCWSTR pszHashItem, int iIndex, UINT uFlags, int iImageIndex)
{
    SHChangeUpdateImageIDList rgPidl;
    SHChangeDWORDAsIDList rgDWord;
    int cchLen;
    USHORT *pcb;

    // Validate parameters: iImageIndex must be a valid system image list value.
    if (iImageIndex < 0)
    {
        return;
    }

    // Validate parameters: pszHashItem must not exceed MAX_PATH in length
    cchLen = lstrlenW(pszHashItem);
    if (cchLen >= MAX_PATH)
    {
        return;
    }

    // Load SHChangeUpdateImageIDList
    rgPidl.dwProcessID = GetCurrentProcessId();
    rgPidl.iIconIndex = iIndex;
    rgPidl.iCurIndex = iImageIndex;
    rgPidl.uFlags = uFlags;
    lstrcpynW(rgPidl.szName, pszHashItem, MAX_PATH);
    pcb = &rgPidl.szName[cchLen+1];
    
    // Set the size of the first element
    rgPidl.cb = (USHORT)((BYTE*)pcb - (BYTE*)rgPidl); 
    
    // Terminate the "ITEMIDLIST"
    *pcb = 0; 

    // Load SHChangeDWORDAsIDList
    rgDWord.cb = (USHORT)FIELD_OFFSET(SHChangeDWORDAsIDList, cbZero);
    rgDWord.dwItem1 = iImageIndex;
    rgDWord.dwItem2 = 0;
    rgDWord.cbZero = 0;

    // Parameters are now in the form that SHCNE_UPDATEIMAGE can accept
    SHChangeNotify(SHCNE_UPDATEIMAGE, SHCNF_IDLIST, &rgDWord, &rgPidl);
}
```

## -see-also

<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangeupdateimageidlist">SHChangeUpdateImageIDList</a>