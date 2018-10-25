---
UID: NS:shlobj_core._SHChangeDWORDAsIDList
title: "_SHChangeDWORDAsIDList"
author: windows-sdk-content
description: SHChangeDWORDAsIDList may be altered or unavailable.
old-location: shell\SHChangeDWORDAsIDList.htm
tech.root: shell
ms.assetid: ebc05a9c-ed2b-41ff-93fb-9d8059fa360c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*LPSHChangeDWORDAsIDList, LPSHChangeDWORDAsIDList, LPSHChangeDWORDAsIDList structure pointer [Windows Shell], SHChangeDWORDAsIDList, SHChangeDWORDAsIDList structure [Windows Shell], _SHChangeDWORDAsIDList, _shell_SHChangeDWORDAsIDList, shell.SHChangeDWORDAsIDList, shlobj_core/LPSHChangeDWORDAsIDList, shlobj_core/SHChangeDWORDAsIDList"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - SHChangeDWORDAsIDList
product: Windows
targetos: Windows
req.typenames: SHChangeDWORDAsIDList, *LPSHChangeDWORDAsIDList
req.redist: 
---

# _SHChangeDWORDAsIDList structure


## -description


<p class="CCE_Message">[<b>SHChangeDWORDAsIDList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Stores two <b>DWORD</b> values in a form mimicking an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> so that they can be used by <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a>.


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



This example demonstrates the use of <a href="https://msdn.microsoft.com/0aa99a6b-39c2-41f3-bd9d-30b86aa4da2f">SHChangeUpdateImageIDList</a> and <b>SHChangeDWORDAsIDList</b> by <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> to mimic the <a href="https://msdn.microsoft.com/9df5860e-db65-4e43-aaf9-c1e0e33fc569">SHUpdateImage</a> function.

                


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




<a href="https://msdn.microsoft.com/0aa99a6b-39c2-41f3-bd9d-30b86aa4da2f">SHChangeUpdateImageIDList</a>
 

 

