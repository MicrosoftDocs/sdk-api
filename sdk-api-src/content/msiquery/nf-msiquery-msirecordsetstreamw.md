---
UID: NF:msiquery.MsiRecordSetStreamW
title: MsiRecordSetStreamW function
author: windows-sdk-content
description: The MsiRecordSetStream function sets a record stream field from a file. Stream data cannot be inserted into temporary fields.
old-location: setup\msirecordsetstream.htm
tech.root: msi
ms.assetid: ca62f6a6-2f39-4b4c-876f-4c74ecd28ee2
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: MsiRecordSetStream, MsiRecordSetStream function, MsiRecordSetStreamA, MsiRecordSetStreamW, _msi_msirecordsetstream, msiquery/MsiRecordSetStream, msiquery/MsiRecordSetStreamA, msiquery/MsiRecordSetStreamW, setup.msirecordsetstream
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
req.unicode-ansi: MsiRecordSetStreamW (Unicode) and MsiRecordSetStreamA (ANSI)
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
 - MsiRecordSetStream
 - MsiRecordSetStreamA
 - MsiRecordSetStreamW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiRecordSetStreamW function


## -description


The 
<b>MsiRecordSetStream</b> function sets a record stream field from a file. Stream data cannot be inserted into temporary fields.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field of the record to set.


### -param szFilePath [in]

Specifies the path to the file containing the stream.


## -returns



The 
<b>MsiRecordSetStream</b> function returns the following values:




## -remarks



The contents of the file specified in the 
<b>MsiRecordSetStream</b> function is read into a stream object. The stream persists if the record is inserted into the database and the database is committed.

To reset the stream to its beginning you must pass in a Null pointer for <i>szFilePath</i>. Do not pass a pointer to an empty string, "", to reset the stream.

See also 
<a href="https://msdn.microsoft.com/ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef">OLE Limitations on Streams</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 

