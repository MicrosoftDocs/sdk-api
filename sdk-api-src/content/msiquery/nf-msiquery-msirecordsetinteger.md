---
UID: NF:msiquery.MsiRecordSetInteger
title: MsiRecordSetInteger function (msiquery.h)
description: Sets a record field to an integer field.helpviewer_keywords: ["MsiRecordSetInteger","MsiRecordSetInteger function","_msi_msirecordsetinteger","msiquery/MsiRecordSetInteger","setup.msirecordsetinteger"]
old-location: setup\msirecordsetinteger.htm
tech.root: Msi
ms.assetid: d95105f0-afd6-4f56-94bd-ac8f49cb8f52
ms.date: 12/05/2018
ms.keywords: MsiRecordSetInteger, MsiRecordSetInteger function, _msi_msirecordsetinteger, msiquery/MsiRecordSetInteger, setup.msirecordsetinteger
f1_keywords:
- msiquery/MsiRecordSetInteger
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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


```cpp
MSIHANDLE hRecord;
UINT lReturn;  

//create an msirecord with no fields
hRecord = MsiCreateRecord(0); 

//attempting to set the first field's value gives you ERROR_INVALID_PARAMETER 
lReturn = MsiRecordSetInteger(hRecord, 1, 0);  

```


To set a record integer field to <b>NULL_INTEGER</b>, set <i>iValue</i> to <b>MSI_NULL_INTEGER</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Record Processing Functions</a>
 

 

