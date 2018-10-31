---
UID: NS:shlobj_core._SHChangeUpdateImageIDList
title: "_SHChangeUpdateImageIDList"
author: windows-sdk-content
description: SHChangeUpdateImageIDList may be altered or unavailable.
old-location: shell\SHChangeUpdateImageIDList.htm
tech.root: shell
ms.assetid: 0aa99a6b-39c2-41f3-bd9d-30b86aa4da2f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPSHChangeUpdateImageIDList, GIL_NOTFILENAME, GIL_SIMULATEDOC, LPSHChangeUpdateImageIDList, LPSHChangeUpdateImageIDList structure pointer [Windows Shell], SHChangeUpdateImageIDList, SHChangeUpdateImageIDList structure [Windows Shell], _SHChangeUpdateImageIDList, _shell_SHChangeUpdateImageIDList, shell.SHChangeUpdateImageIDList, shlobj_core/LPSHChangeUpdateImageIDList, shlobj_core/SHChangeUpdateImageIDList"
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
 - SHChangeUpdateImageIDList
product: Windows
targetos: Windows
req.typenames: SHChangeUpdateImageIDList, *LPSHChangeUpdateImageIDList
req.redist: 
---

# _SHChangeUpdateImageIDList structure


## -description


<p class="CCE_Message">[<b>SHChangeUpdateImageIDList</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Stores the information used as parameters to <a href="https://msdn.microsoft.com/9df5860e-db65-4e43-aaf9-c1e0e33fc569">SHUpdateImage</a> in a form mimicking an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> so that they can be used by <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a>.


## -struct-fields




### -field cb

Type: <b>USHORT</b>

The size of the structure, in bytes.


### -field iIconIndex

Type: <b>int</b>

The zero-based index of the icon in the file specified by <b>szName</b>. Obtain this value by calling <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> and retrieving the value pointed to by <i>piIndex</i>.


### -field iCurIndex

Type: <b>int</b>

The zero-based index in the system image list of the icon being updated.


### -field uFlags

Type: <b>UINT</b>

Flags that determine the icon attributes. Obtain this value by calling <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> and retrieving the value pointed to by <i>pwFlags</i>. These two flags are relevant to <a href="https://msdn.microsoft.com/9df5860e-db65-4e43-aaf9-c1e0e33fc569">SHUpdateImage</a>.



#### GIL_NOTFILENAME

The location is not a file name/index pair. Calling applications that decide to extract the icon from the location must call this object's <a href="https://msdn.microsoft.com/3ce54876-e4f8-4f9a-8e1c-ec1db691f020">IExtractIcon::Extract</a> method to obtain the desired icon images.



#### GIL_SIMULATEDOC

The calling application should create a document icon using the specified icon.


### -field dwProcessID

 


### -field szName

Type: <b>WCHAR[MAX_PATH]</b>

A null-terminated Unicode string that specifies the fully qualified path of the file that contains the icon. Obtain this value by calling <a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a> and retrieving the value pointed to by <i>szIconFile</i>.


### -field cbZero

Type: <b>USHORT</b>


#### - dwProcessIDint

Type: <b>DWORD</b>

The identifier of the process sending the SHCNE_UPDATEIMAGE notification.


## -remarks



This example demonstrates the use of <b>SHChangeUpdateImageIDList</b> and <a href="https://msdn.microsoft.com/ebc05a9c-ed2b-41ff-93fb-9d8059fa360c">SHChangeDWORDAsIDList</a> by <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> to mimic the <a href="https://msdn.microsoft.com/9df5860e-db65-4e43-aaf9-c1e0e33fc569">SHUpdateImage</a> function.

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>void MyUpdateImage(LPCWSTR pszHashItem, int iIndex, UINT uFlags, int iImageIndex)
{
    SHChangeUpdateImageIDList rgPidl;
    SHChangeDWORDAsIDList rgDWord;
    int cchLen;
    USHORT *pcb;

    // Validate parameters: iImageIndex must be a valid system image list value.
    if (iImageIndex &lt; 0)
    {
        return;
    }

    // Validate parameters: pszHashItem must not exceed MAX_PATH in length
    cchLen = lstrlenW(pszHashItem);
    if (cchLen &gt;= MAX_PATH)
    {
        return;
    }

    // Load SHChangeUpdateImageIDList
    rgPidl.dwProcessID = GetCurrentProcessId();
    rgPidl.iIconIndex = iIndex;
    rgPidl.iCurIndex = iImageIndex;
    rgPidl.uFlags = uFlags;
    lstrcpynW(rgPidl.szName, pszHashItem, MAX_PATH);
    pcb = &amp;amp;rgPidl.szName[cchLen+1];
    
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
    SHChangeNotify(SHCNE_UPDATEIMAGE, SHCNF_IDLIST, &amp;rgDWord, &amp;rgPidl);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/56138982-c062-4b07-aea7-6023037451fe">IExtractIcon::GetIconLocation</a>



<a href="https://msdn.microsoft.com/ebc05a9c-ed2b-41ff-93fb-9d8059fa360c">SHChangeDWORDAsIDList</a>
 

 

