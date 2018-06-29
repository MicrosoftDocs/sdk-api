---
UID: NF:msiquery.MsiRecordSetStringA
title: MsiRecordSetStringA function
author: windows-sdk-content
description: The MsiRecordSetString function copies a string into the designated field.
old-location: setup\msirecordsetstring.htm
old-project: Msi
ms.assetid: 225454be-b653-4679-ae77-2280bd3c8d69
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: MsiRecordSetString, MsiRecordSetString function, MsiRecordSetStringA, MsiRecordSetStringW, _msi_msirecordsetstring, msiquery/MsiRecordSetString, msiquery/MsiRecordSetStringA, msiquery/MsiRecordSetStringW, setup.msirecordsetstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiRecordSetStringW (Unicode) and MsiRecordSetStringA (ANSI)
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
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiRecordSetString
 - MsiRecordSetStringA
 - MsiRecordSetStringW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiRecordSetStringA function


## -description


The 
<b>MsiRecordSetString</b> function copies a string into the designated field.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field of the record to set.


### -param szValue [in]

Specifies the string value of the field.


## -returns



This function returns UINT.




## -remarks



In the 
<b>MsiRecordSetString</b> function, a null string pointer and an empty string both set the field to null. Attempting to store a value in a nonexistent field causes an error.

To set a record string field to null, set szValue to either a null string or an empty string.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa368250(v=VS.85).aspx">Record Processing Functions</a>
 

 

