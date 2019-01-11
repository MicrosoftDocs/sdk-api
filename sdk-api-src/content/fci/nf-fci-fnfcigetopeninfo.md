---
UID: NF:fci.FNFCIGETOPENINFO
title: FNFCIGETOPENINFO macro
author: windows-sdk-content
description: The FNFCIGETOPENINFO macro provides the declaration for the application-defined callback function to open a file and retrieve file date, time, and attribute.
old-location: winprog\fnfcigetopeninfo.htm
tech.root: DevNotes
ms.assetid: 5baccb69-7872-4d67-ad74-70cdd7459f8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FNFCIGETOPENINFO, FNFCIGETOPENINFO macro [Windows API], fci/FNFCIGETOPENINFO, winprog.fnfcigetopeninfo
ms.topic: macro
req.header: fci.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - fci.h
api_name:
 - FNFCIGETOPENINFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FNFCIGETOPENINFO macro


## -description


The <b>FNFCIGETOPENINFO</b> macro provides the declaration for the application-defined callback function to open a file and retrieve file date, time, and attribute.


## -parameters




### -param fn [in]

 The complete filename.


#### - err

Pointer to the error code value. This value will be used to provide extended error information in the <a href="https://msdn.microsoft.com/en-us/library/Bb432257(v=VS.85).aspx">ERF</a> structure used to create the FCI context.


#### - pattribs

The file attributes. For possible values and their descriptions, see File Attributes.


#### - pdate

 The MS-DOS date. The date is a packed value with the following format:

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Day of the Month (1-31)</td>
</tr>
<tr>
<td>5-8</td>
<td>Month (1 = January, 2 = Feburary, etc.)</td>
</tr>
<tr>
<td>9-15</td>
<td>Year Offset from 1980 (add 1980 to value to get current date)</td>
</tr>
</table>
 


#### - ptime

The MS-DOS time. The time is a packed value with the following format:

<table>
<tr>
<th>Bits</th>
<th>Description</th>
</tr>
<tr>
<td>0-4</td>
<td>Second divided by 2</td>
</tr>
<tr>
<td>5-8</td>
<td>Minute (0-59)</td>
</tr>
<tr>
<td>9-15</td>
<td>Hour (0-23 on a 24-hour clock)</td>
</tr>
</table>
 


#### - pv

Pointer to an application-defined value.


## -remarks



The function should open the file using the file open function compatible with those passed into <a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIGETOPENINFO(fnGetOpenInfo)
{
    HANDLE hFile;
    FILETIME fileTime;
    BY_HANDLE_FILE_INFORMATION fileInfo;

    hFile = (HANDLE)fnFileOpen(pszName, _O_RDONLY, 0, err, pv);

    if ( hFile != (HANDLE)-1 )
    {
        if( GetFileInformationByHandle(hFile, &amp;fileInfo) 
        &amp;&amp;  FileTimeToLocalFileTime(&amp;fileInfo.ftCreationTime, &amp;fileTime)
        &amp;&amp;  FileTimeToDosDateTime(&amp;fileTime, pdate, ptime) )
        {
            *pattribs = (USHORT)fileInfo.dwFileAttributes;
            *pattribs &amp;= ( _A_RDONLY | _A_HIDDEN | _A_SYSTEM | _A_ARCH );
        }
        else
        {
            fnFileClose((INT_PTR)hFile, err, pv);
            hFile = (HANDLE)-1;
        }
    }

    return (INT_PTR)hFile;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

