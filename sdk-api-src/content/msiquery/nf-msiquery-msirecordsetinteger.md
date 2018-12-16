---
UID: NF:msiquery.MsiRecordSetInteger
title: MsiRecordSetInteger function
author: windows-sdk-content
description: Sets a record field to an integer field.
old-location: setup\msirecordsetinteger.htm
tech.root: msi
ms.assetid: d95105f0-afd6-4f56-94bd-ac8f49cb8f52
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MsiRecordSetInteger, MsiRecordSetInteger function, _msi_msirecordsetinteger, msiquery/MsiRecordSetInteger, setup.msirecordsetinteger
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista.
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiRecordSetInteger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiRecordSetInteger function


## -description


The 
<b>MsiRecordSetInteger</b> function sets a record field to an integer field.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field of the record to set.


### -param iValue [in]

Specifies the value to which to set the field.


## -returns



This function returns UINT.




## -remarks



In the 
<b>MsiRecordSetInteger</b> function, attempting to store a value in a nonexistent field causes an error. Note that the following code returns <b>ERROR_INVALID_PARAMETER</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>MSIHANDLE hRecord;
UINT lReturn;  

//create an msirecord with no fields
hRecord = MsiCreateRecord(0); 

//attempting to set the first field's value gives you ERROR_INVALID_PARAMETER 
lReturn = MsiRecordSetInteger(hRecord, 1, 0);  
</pre>
</td>
</tr>
</table></span></div>
To set a record integer field to <b>NULL_INTEGER</b>, set <i>iValue</i> to <b>MSI_NULL_INTEGER</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Record Processing Functions</a>
 

 

