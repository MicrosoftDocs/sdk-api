---
UID: NS:wtypesbase.tagBLOB
title: BLOB (wtypesbase.h)
description: The BLOB (wtypesbase.h) structure, derived from Binary Large Object, contains information about a block of data.
helpviewer_keywords: ["*LPBLOB","BLOB","BLOB structure [Winsock]","_win32_blob_2","tagBLOB","winsock.blob_2","wtypesbase/BLOB"]
old-location: winsock\blob_2.htm
tech.root: WinSock
ms.assetid: eb1ff7d1-79db-478f-9f3e-48507d333c76
ms.date: 08/16/2022
ms.keywords: '*LPBLOB, BLOB, BLOB structure [Winsock], _win32_blob_2, tagBLOB, winsock.blob_2, wtypesbase/BLOB'
req.header: wtypesbase.h
req.include-header: Wtypes.h, Nspapi.h, Winsock2.h, Wtypes.h, Nspapi.h, Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BLOB, *LPBLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagBLOB
 - wtypesbase/tagBLOB
 - LPBLOB
 - wtypesbase/LPBLOB
 - BLOB
 - wtypesbase/BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wtypesbase.h
api_name:
 - BLOB
---

# BLOB structure


## -description

The 
<b>BLOB</b> structure, derived from Binary Large Object, contains information about a block of data.

## -struct-fields

### -field cbSize

Size of the block of data pointed to by <b>pBlobData</b>, in bytes.

### -field pBlobData

Pointer to a block of data.

## -remarks

The structure name 
<b>BLOB</b> comes from the acronym BLOB, which stands for Binary Large Object.

This structure does not describe the nature of the data pointed to by <b>pBlobData</b>.

<div class="alert"><b>Note</b>  Windows Sockets defines a similar 
<b>BLOB</b> structure in Wtypes.h. Using both header files in the same source code file creates redefinition–compile time errors.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-blob">Bluetooth and BLOB</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>
