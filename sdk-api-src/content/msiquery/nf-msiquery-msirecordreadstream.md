---
UID: NF:msiquery.MsiRecordReadStream
title: MsiRecordReadStream function (msiquery.h)
description: The MsiRecordReadStream function reads bytes from a record stream field into a buffer.
helpviewer_keywords: ["MsiRecordReadStream","MsiRecordReadStream function","_msi_msirecordreadstream","msiquery/MsiRecordReadStream","setup.msirecordreadstream"]
old-location: setup\msirecordreadstream.htm
tech.root: setup
ms.assetid: a7ff84f0-15d2-4fb2-98c7-8fb8d2f14004
ms.date: 12/05/2018
ms.keywords: MsiRecordReadStream, MsiRecordReadStream function, _msi_msirecordreadstream, msiquery/MsiRecordReadStream, setup.msirecordreadstream
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
 - MsiRecordReadStream
 - msiquery/MsiRecordReadStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiRecordReadStream
---

# MsiRecordReadStream function


## -description

The 
<b>MsiRecordReadStream</b> function reads bytes from a record stream field into a buffer.

## -parameters

### -param hRecord [in]

Handle to the record.

### -param iField [in]

Specifies the field of the record.

### -param szDataBuf [out]

A buffer to receive the stream field. You should ensure the destination buffer is the same size or larger than the source buffer. See the Remarks section.

### -param pcbDataBuf [in, out]

Specifies the in and out buffer count. On input, this is the full size of the buffer. On output, this is the number of bytes that were actually written to the buffer. See the Remarks section.

## -returns

This function returns UINT.

## -remarks

To read a stream, set <i>pcbDataBuf</i> to the number of bytes that are to be transferred from stream to buffer each time the function is called. On return, the 
<b>MsiRecordReadStream</b> resets <i>pcbDataBuf </i> to the number of bytes that were actually transferred. If the buffer is smaller than the stream, the stream is repositioned when the buffer becomes full such that the next data in the stream is transferred by the next call to the function. When no more bytes are available, 
<b>MsiRecordReadStream</b> returns ERROR_SUCCESS.

If you pass 0 for <i>szDataBuf</i> then <i>pcbDataBuf</i> is reset to the number of bytes in the stream remaining to be read.

The following code sample reads from a stream that is in field 1 of a record specified by hRecord and reads the entire stream 8 bytes at a time.


```cpp
char szBuffer[8];
PMSIHANDLE hRecord;
DWORD cbBuf = sizeof(szBuffer);
do 
{
    if (MsiRecordReadStream(hRecord, 1, szBuffer, 
        &cbBuf) != ERROR_SUCCESS)
        break; /* error */
}
while (cbBuf == 8);  //continue reading the stream while you receive a full buffer
//cbBuf will be less once you reach the end of the stream and cannot fill your 
//buffer with stream data

```


See also 
<a href="/windows/desktop/Msi/ole-limitations-on-streams">OLE Limitations on Streams</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">Record Processing Functions</a>