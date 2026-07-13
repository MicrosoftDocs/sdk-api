---
UID: NF:msiquery.MsiRecordSetStreamW
title: MsiRecordSetStreamW function (msiquery.h)
description: The MsiRecordSetStream function sets a record stream field from a file. Stream data cannot be inserted into temporary fields. (Unicode)
helpviewer_keywords: ["MsiRecordSetStream", "MsiRecordSetStream function", "MsiRecordSetStreamW", "_msi_msirecordsetstream", "msiquery/MsiRecordSetStream", "msiquery/MsiRecordSetStreamW", "setup.msirecordsetstream"]
old-location: setup\msirecordsetstream.htm
tech.root: setup
ms.assetid: ca62f6a6-2f39-4b4c-876f-4c74ecd28ee2
ms.date: 12/05/2018
ms.keywords: MsiRecordSetStream, MsiRecordSetStream function, MsiRecordSetStreamA, MsiRecordSetStreamW, _msi_msirecordsetstream, msiquery/MsiRecordSetStream, msiquery/MsiRecordSetStreamA, msiquery/MsiRecordSetStreamW, setup.msirecordsetstream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiRecordSetStreamW
 - msiquery/MsiRecordSetStreamW
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
 - MsiRecordSetStream
 - MsiRecordSetStreamA
 - MsiRecordSetStreamW
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
<a href="/windows/desktop/Msi/ole-limitations-on-streams">OLE Limitations on Streams</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiRecordSetStream as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>
