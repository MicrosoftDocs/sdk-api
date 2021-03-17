---
UID: NF:msiquery.MsiRecordIsNull
title: MsiRecordIsNull function (msiquery.h)
description: Reports a null record field.
helpviewer_keywords: ["MsiRecordIsNull","MsiRecordIsNull function","_msi_msirecordisnull","msiquery/MsiRecordIsNull","setup.msirecordisnull"]
old-location: setup\msirecordisnull.htm
tech.root: setup
ms.assetid: e37a458c-8868-4f8c-96fd-a713d2a9c5ad
ms.date: 12/05/2018
ms.keywords: MsiRecordIsNull, MsiRecordIsNull function, _msi_msirecordisnull, msiquery/MsiRecordIsNull, setup.msirecordisnull
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiRecordIsNull
 - msiquery/MsiRecordIsNull
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
 - MsiRecordIsNull
---

# MsiRecordIsNull function


## -description

The 
<b>MsiRecordIsNull</b> function reports a null record field.

## -parameters

### -param hRecord [in]

Handle to a record.

### -param iField [in]

Specifies the field to check.

## -returns

This function returns BOOL.

## -remarks

The <i>iField</i> parameter is based on 1 (one).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>