---
UID: NS:shlobj_core._SHChangeUpdateImageIDList
title: SHChangeUpdateImageIDList (shlobj_core.h)
description: SHChangeUpdateImageIDList may be altered or unavailable.
helpviewer_keywords: ["*LPSHChangeUpdateImageIDList","GIL_NOTFILENAME","GIL_SIMULATEDOC","LPSHChangeUpdateImageIDList","LPSHChangeUpdateImageIDList structure pointer [Windows Shell]","SHChangeUpdateImageIDList","SHChangeUpdateImageIDList structure [Windows Shell]","_SHChangeUpdateImageIDList","_shell_SHChangeUpdateImageIDList","shell.SHChangeUpdateImageIDList","shlobj_core/LPSHChangeUpdateImageIDList","shlobj_core/SHChangeUpdateImageIDList"]
old-location: shell\SHChangeUpdateImageIDList.htm
tech.root: shell
ms.assetid: 0aa99a6b-39c2-41f3-bd9d-30b86aa4da2f
ms.date: 12/05/2018
ms.keywords: '*LPSHChangeUpdateImageIDList, GIL_NOTFILENAME, GIL_SIMULATEDOC, LPSHChangeUpdateImageIDList, LPSHChangeUpdateImageIDList structure pointer [Windows Shell], SHChangeUpdateImageIDList, SHChangeUpdateImageIDList structure [Windows Shell], _SHChangeUpdateImageIDList, _shell_SHChangeUpdateImageIDList, shell.SHChangeUpdateImageIDList, shlobj_core/LPSHChangeUpdateImageIDList, shlobj_core/SHChangeUpdateImageIDList'
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
req.typenames: SHChangeUpdateImageIDList, *LPSHChangeUpdateImageIDList
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHChangeUpdateImageIDList
 - shlobj_core/_SHChangeUpdateImageIDList
 - LPSHChangeUpdateImageIDList
 - shlobj_core/LPSHChangeUpdateImageIDList
 - SHChangeUpdateImageIDList
 - shlobj_core/SHChangeUpdateImageIDList
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
 - SHChangeUpdateImageIDList
---

# SHChangeUpdateImageIDList structure


## -description

<p class="CCE_Message">[<b>SHChangeUpdateImageIDList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Stores the information used as parameters to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea">SHUpdateImage</a> in a form mimicking an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> so that they can be used by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a>.

## -struct-fields

### -field cb

Type: <b>USHORT</b>

The size of the structure, in bytes.

### -field iIconIndex

Type: <b>int</b>

The zero-based index of the icon in the file specified by <b>szName</b>. Obtain this value by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> and retrieving the value pointed to by <i>piIndex</i>.

### -field iCurIndex

Type: <b>int</b>

The zero-based index in the system image list of the icon being updated.

### -field uFlags

Type: <b>UINT</b>

Flags that determine the icon attributes. Obtain this value by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> and retrieving the value pointed to by <i>pwFlags</i>. These two flags are relevant to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea">SHUpdateImage</a>.



#### GIL_NOTFILENAME

The location is not a file name/index pair. Calling applications that decide to extract the icon from the location must call this object's <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-extract">IExtractIcon::Extract</a> method to obtain the desired icon images.



#### GIL_SIMULATEDOC

The calling application should create a document icon using the specified icon.

### -field dwProcessID

### -field szName

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string that specifies the fully qualified path of the file that contains the icon. Obtain this value by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a> and retrieving the value pointed to by <i>szIconFile</i>.

### -field cbZero

Type: <b>USHORT</b>


#### - dwProcessIDint

Type: <b>DWORD</b>

The identifier of the process sending the SHCNE_UPDATEIMAGE notification.

## -remarks

This example demonstrates the use of <b>SHChangeUpdateImageIDList</b> and <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangedwordasidlist">SHChangeDWORDAsIDList</a> by <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify">SHChangeNotify</a> to mimic the <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea">SHUpdateImage</a> function.

                


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

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">IExtractIcon::GetIconLocation</a>



<a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangedwordasidlist">SHChangeDWORDAsIDList</a>