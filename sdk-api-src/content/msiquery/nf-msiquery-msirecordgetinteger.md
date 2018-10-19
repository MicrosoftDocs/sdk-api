---
UID: NF:msiquery.MsiRecordGetInteger
title: MsiRecordGetInteger function
author: windows-sdk-content
description: The MsiRecordGetInteger function returns the integer value from a record field.
old-location: setup\msirecordgetinteger.htm
tech.root: msi
ms.assetid: f04d4d61-ebe0-4eb1-b0e7-b94d9ef3c900
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: MsiRecordGetInteger, MsiRecordGetInteger function, _msi_msirecordgetinteger, msiquery/MsiRecordGetInteger, setup.msirecordgetinteger
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MsiRecordGetInteger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiRecordGetInteger function


## -description


The 
<b>MsiRecordGetInteger</b> function returns the integer value from a record field.


## -parameters




### -param hRecord [in]

Handle to a record.


### -param iField [in]

Specifies the field of the record from which to obtain the value.


## -returns



If the function succeeds, the return value is the integer value of the field.




## -remarks



The 
<b>MsiRecordGetInteger</b> function returns <b>MSI_NULL_INTEGER</b> if the field is null or if the field is a string that cannot be converted to an integer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Record Processing Functions</a>
 

 

