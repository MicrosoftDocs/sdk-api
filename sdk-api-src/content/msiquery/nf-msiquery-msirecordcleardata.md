---
UID: NF:msiquery.MsiRecordClearData
title: MsiRecordClearData function (msiquery.h)
description: The MsiRecordClearData function sets all fields in a record to null.
helpviewer_keywords: ["MsiRecordClearData","MsiRecordClearData function","_msi_msirecordcleardata","msiquery/MsiRecordClearData","setup.msirecordcleardata"]
old-location: setup\msirecordcleardata.htm
tech.root: setup
ms.assetid: 61fc362e-2b8e-4ce4-83e2-bade40fb96bc
ms.date: 12/05/2018
ms.keywords: MsiRecordClearData, MsiRecordClearData function, _msi_msirecordcleardata, msiquery/MsiRecordClearData, setup.msirecordcleardata
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiRecordClearData
 - msiquery/MsiRecordClearData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiRecordClearData
---

# MsiRecordClearData function


## -description

The 
<b>MsiRecordClearData</b> function sets all fields in a record to null.

## -parameters

### -param hRecord [in]

Handle to the record.

## -returns

This function returns UINT.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>