---
UID: NF:msiquery.MsiRecordGetStringA
title: MsiRecordGetStringA function
author: windows-sdk-content
description: The MsiRecordGetString function returns the string value of a record field.
old-location: setup\msirecordgetstring.htm
old-project: msi
ms.assetid: 4d1b049c-9511-4858-8cc1-3cd2424c55ca
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: MsiRecordGetString, MsiRecordGetString function, MsiRecordGetStringA, MsiRecordGetStringW, _msi_msirecordgetstring, msiquery/MsiRecordGetString, msiquery/MsiRecordGetStringA, msiquery/MsiRecordGetStringW, setup.msirecordgetstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiRecordGetStringW (Unicode) and MsiRecordGetStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InkRecoGuide
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiRecordGetString
 - MsiRecordGetStringA
 - MsiRecordGetStringW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiRecordGetStringA function


## -description


The 
<b>MsiRecordGetString</b> function returns the string value of a record field.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field requested.


### -param szValueBuf [out]

Pointer to the buffer that receives the null terminated string containing the value of the record field. Do not attempt to determine the size of the buffer by passing in a null (value=0) for <i>szValueBuf</i>. You can get the size of the buffer by passing in an empty string (for example ""). The function then returns <b>ERROR_MORE_DATA</b> and <i>pcchValueBuf</i> contains the required buffer size in TCHARs, not including the terminating null character. On return of <b>ERROR_SUCCESS</b>, <i>pcchValueBuf</i> contains the number of <b>TCHARs</b> written to the buffer, not including the terminating null character.


### -param pcchValueBuf [in, out]

Pointer to the variable that specifies the size, in <b>TCHAR</b>s, of the buffer pointed to by the variable <i>szValueBuf</i>. When the function returns <b>ERROR_SUCCESS</b>, this variable contains the size of the data copied to <i>szValueBuf</i>, not including the terminating null character. If <i>szValueBuf</i> is not large enough, the function returns <b>ERROR_MORE_DATA</b> and stores the required size, not including the terminating null character, in the variable pointed to by <i>pcchValueBuf</i>.


## -returns



The 
<b>MsiRecordGetString</b> function returns one of the following values:




## -remarks



If <b>ERROR_MORE_DATA</b> is returned, the parameter which is a pointer gives the size of the buffer required to hold the string. If <b>ERROR_SUCCESS</b> is returned, it gives the number of characters written to the string buffer. To get the size of the buffer, pass in the address of a 1 character buffer as <i>szValueBuf</i> and specify the size of the buffer with <i>pcchValueBuf</i> as 0. This ensures that no string value returned by the function fits into the buffer. Do not attempt to determine the size of the buffer by passing in a Null (value=0).




## -see-also




<a href="https://msdn.microsoft.com/f566c4a4-b90c-4d73-9d7f-f5b836630636">Passing Null as the Argument of Windows Installer Functions</a>



<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">Record Processing Functions</a>
 

 

