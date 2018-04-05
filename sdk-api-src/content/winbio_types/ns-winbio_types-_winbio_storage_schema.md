---
UID: NS:winbio_types._WINBIO_STORAGE_SCHEMA
title: "_WINBIO_STORAGE_SCHEMA"
author: windows-driver-content
description: Describes the capabilities of a biometric storage adapter.
old-location: secbiomet\winbio_storage_schema.htm
old-project: SecBioMet
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_STORAGE_SCHEMA, PWINBIO_STORAGE_SCHEMA, PWINBIO_STORAGE_SCHEMA structure pointer [Windows Biometric Framework API], WINBIO_DATABASE_FLAG_MASK, WINBIO_DATABASE_FLAG_REMOTE, WINBIO_DATABASE_FLAG_REMOVABLE, WINBIO_DATABASE_TYPE_DBMS, WINBIO_DATABASE_TYPE_FILE, WINBIO_DATABASE_TYPE_MASK, WINBIO_DATABASE_TYPE_ONCHIP, WINBIO_DATABASE_TYPE_SMARTCARD, WINBIO_STORAGE_SCHEMA, WINBIO_STORAGE_SCHEMA structure [Windows Biometric Framework API], _WINBIO_STORAGE_SCHEMA, secbiomet.winbio_storage_schema, winbio_types/PWINBIO_STORAGE_SCHEMA, winbio_types/WINBIO_STORAGE_SCHEMA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_types.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_STORAGE_SCHEMA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_STORAGE_SCHEMA structure


## -description


The <b>WINBIO_STORAGE_SCHEMA</b> structure describes the capabilities of a biometric storage adapter. This structure is used by the <a href="https://msdn.microsoft.com/163c669d-765f-4f8d-83c4-ff8bd064e44d">WinBioEnumDatabases</a> function.


## -struct-fields




### -field BiometricFactor

The type of biometric measurement saved in the database.


### -field DatabaseId

A GUID that identifies the database.


### -field DataFormat

A GUID that identifies the format of the templates in the database.


### -field Attributes

Information about the characteristics of the database. This can be a bitwise <b>OR</b> of the following constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_FLAG_MASK"></a><a id="winbio_database_flag_mask"></a><dl>
<dt><b>WINBIO_DATABASE_FLAG_MASK</b></dt>
<dt>0xFFFF0000</dt>
</dl>
</td>
<td width="60%">
Represents a mask for the flag bits.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_FLAG_REMOTE"></a><a id="winbio_database_flag_remote"></a><dl>
<dt><b>WINBIO_DATABASE_FLAG_REMOTE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The database resides on a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_FLAG_REMOVABLE"></a><a id="winbio_database_flag_removable"></a><dl>
<dt><b>WINBIO_DATABASE_FLAG_REMOVABLE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
The database resides on a removable drive.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_TYPE_DBMS"></a><a id="winbio_database_type_dbms"></a><dl>
<dt><b>WINBIO_DATABASE_TYPE_DBMS</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The database is managed by a database management system.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_TYPE_FILE"></a><a id="winbio_database_type_file"></a><dl>
<dt><b>WINBIO_DATABASE_TYPE_FILE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The database is contained in a file.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_TYPE_MASK"></a><a id="winbio_database_type_mask"></a><dl>
<dt><b>WINBIO_DATABASE_TYPE_MASK</b></dt>
<dt>0x0000FFFF</dt>
</dl>
</td>
<td width="60%">
Represents a mask for the type bits.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_TYPE_ONCHIP"></a><a id="winbio_database_type_onchip"></a><dl>
<dt><b>WINBIO_DATABASE_TYPE_ONCHIP</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The database resides on the biometric sensor.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_DATABASE_TYPE_SMARTCARD"></a><a id="winbio_database_type_smartcard"></a><dl>
<dt><b>WINBIO_DATABASE_TYPE_SMARTCARD</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The database resides on a smart card.

</td>
</tr>
</table>
 


### -field FilePath

The path and file name of the database if it resides on the computer disk.


### -field ConnectionString

A string value that can be sent to a database server to identify the database.


## -see-also




<a href="https://msdn.microsoft.com/ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73">Client Application Structures</a>



<a href="https://msdn.microsoft.com/163c669d-765f-4f8d-83c4-ff8bd064e44d">WinBioEnumDatabases</a>
 

 

