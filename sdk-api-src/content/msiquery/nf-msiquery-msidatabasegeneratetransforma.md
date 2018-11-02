---
UID: NF:msiquery.MsiDatabaseGenerateTransformA
title: MsiDatabaseGenerateTransformA function
author: windows-sdk-content
description: The MsiDatabaseGenerateTransform function generates a transform file of differences between two databases.
old-location: setup\msidatabasegeneratetransform.htm
tech.root: msi
ms.assetid: 9e8fc756-4195-4fb7-9adb-0bda20e4ae95
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MsiDatabaseGenerateTransform, MsiDatabaseGenerateTransform function, MsiDatabaseGenerateTransformA, MsiDatabaseGenerateTransformW, _msi_msidatabasegeneratetransform, msiquery/MsiDatabaseGenerateTransform, msiquery/MsiDatabaseGenerateTransformA, msiquery/MsiDatabaseGenerateTransformW, setup.msidatabasegeneratetransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDatabaseGenerateTransformW (Unicode) and MsiDatabaseGenerateTransformA (ANSI)
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
api_name:
 - MsiDatabaseGenerateTransform
 - MsiDatabaseGenerateTransformA
 - MsiDatabaseGenerateTransformW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiDatabaseGenerateTransformA function


## -description


The 
<b>MsiDatabaseGenerateTransform</b> function generates a transform file of differences between two databases. A transform is a way of recording changes to a database without altering the original database. You can also use 
<b>MsiDatabaseGenerateTransform</b> to test whether two databases are identical without creating a transform.


## -parameters




### -param hDatabase [in]

Handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a> that includes the changes.


### -param hDatabaseReference [in]

Handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a> that does not include the changes.


### -param szTransformFile [in]

A null-terminated string that specifies the name of the transform file being generated. This parameter can be null. If <i>szTransformFile</i> is null, you can use 
<b>MsiDatabaseGenerateTransform</b> to test whether two databases are identical without creating a transform. If the databases are identical, the function returns ERROR_NO_DATA. If the databases are different the function returns NOERROR.


### -param iReserved1 [in]

This is a reserved argument and must be set to 0.


### -param iReserved2 [in]

This is a reserved argument and must be set to 0.


## -returns



The 
<b>MsiDatabaseGenerateTransform</b> function returns one of the following values:




## -remarks



To generate a difference file between two databases, use the 
<b>MsiDatabaseGenerateTransform</b> function. A transform contains information regarding insertion and deletion of columns and rows. The validation flags are stored in the summary information stream of the transform file.

For tables that exist in both databases, the only difference between the two schemas that is allowed is the addition of columns to the end of the reference table. You cannot add primary key columns to a table or change the order or names or column definitions of the existing columns as defined in the base table. In other words, if neither table contains data and columns are removed from the reference table, the resulting table is identical to the base table.

Because the list delimiter for transforms, sources and patches is a semicolon, this character should not be used for filenames or paths.

This function does not generate a Summary Information stream. Use 
<a href="https://msdn.microsoft.com/7ed6738c-f693-477e-a3d7-e4f50d222fdb">MsiCreateTransformSummaryInfo</a> to create the stream for an existing transform.

If <i>szTransformFile</i> is null, you can test whether two databases are identical without creating a transform. If the databases are identical, ERROR_NO_DATA is returned, NOERROR is returned if differences are found.

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa368250(v=VS.85).aspx">Database Management Functions</a>



<a href="https://msdn.microsoft.com/525feb70-27aa-4fe2-a19f-9438168ca046">Database Transforms</a>
 

 

