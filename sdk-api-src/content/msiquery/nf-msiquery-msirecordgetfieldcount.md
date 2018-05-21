---
UID: NF:msiquery.MsiRecordGetFieldCount
title: MsiRecordGetFieldCount function
author: windows-driver-content
description: Returns the number of fields in a record.
old-location: setup\msirecordgetfieldcount.htm
old-project: Msi
ms.assetid: 17d4e593-f80c-4f67-bfd0-fa487e2477c4
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: MsiRecordGetFieldCount, MsiRecordGetFieldCount function, _msi_msirecordgetfieldcount, msiquery/MsiRecordGetFieldCount, setup.msirecordgetfieldcount
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
req.typenames: InkRecoGuide
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
-	Ext-MS-Win-MSi-Misc-L1-1-0.dll
api_name:
-	MsiRecordGetFieldCount
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# MsiRecordGetFieldCount function


## -description


The 
<b>MsiRecordGetFieldCount</b> function returns the number of fields in a record.


## -parameters




### -param hRecord [in]

Handle to a record.


## -returns



If the function succeeds, the return value is the number of fields in the record.




## -remarks



The count returned by the 
<b>MsiRecordGetFieldCount</b> parameter does not include field 0. Read access to fields beyond this count returns null values. Write access fails.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

