---
UID: NE:msrdc.__MIDL___MIDL_itf_msrdc_0000_0000_0001
title: RDC_ErrorCode (msrdc.h)
description: Defines the set of RDC-specific error codes.
helpviewer_keywords: ["RDC_Aborted","RDC_ApplicationError","RDC_DataMissingOrCorrupt","RDC_DataTooManyRecords","RDC_ErrorCode","RDC_ErrorCode enumeration [Remote Differential Compression]","RDC_FileChecksumMismatch","RDC_HeaderMissingOrCorrupt","RDC_HeaderVersionNewer","RDC_HeaderVersionOlder","RDC_HeaderWrongType","RDC_NoError","RDC_Win32Error","fs.rdc_errorcode","msrdc/RDC_Aborted","msrdc/RDC_ApplicationError","msrdc/RDC_DataMissingOrCorrupt","msrdc/RDC_DataTooManyRecords","msrdc/RDC_ErrorCode","msrdc/RDC_FileChecksumMismatch","msrdc/RDC_HeaderMissingOrCorrupt","msrdc/RDC_HeaderVersionNewer","msrdc/RDC_HeaderVersionOlder","msrdc/RDC_HeaderWrongType","msrdc/RDC_NoError","msrdc/RDC_Win32Error","rdc.rdc_errorcode"]
old-location: rdc\rdc_errorcode.htm
tech.root: rdc
ms.assetid: 32e9eab0-dc6e-4e04-af8a-bc2ed4adf0be
ms.date: 12/05/2018
ms.keywords: RDC_Aborted, RDC_ApplicationError, RDC_DataMissingOrCorrupt, RDC_DataTooManyRecords, RDC_ErrorCode, RDC_ErrorCode enumeration [Remote Differential Compression], RDC_FileChecksumMismatch, RDC_HeaderMissingOrCorrupt, RDC_HeaderVersionNewer, RDC_HeaderVersionOlder, RDC_HeaderWrongType, RDC_NoError, RDC_Win32Error, fs.rdc_errorcode, msrdc/RDC_Aborted, msrdc/RDC_ApplicationError, msrdc/RDC_DataMissingOrCorrupt, msrdc/RDC_DataTooManyRecords, msrdc/RDC_ErrorCode, msrdc/RDC_FileChecksumMismatch, msrdc/RDC_HeaderMissingOrCorrupt, msrdc/RDC_HeaderVersionNewer, msrdc/RDC_HeaderVersionOlder, msrdc/RDC_HeaderWrongType, msrdc/RDC_NoError, msrdc/RDC_Win32Error, rdc.rdc_errorcode
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RDC_ErrorCode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msrdc_0000_0000_0001
 - msrdc/__MIDL___MIDL_itf_msrdc_0000_0000_0001
 - RDC_ErrorCode
 - msrdc/RDC_ErrorCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsRdc.h
api_name:
 - RDC_ErrorCode
---

# RDC_ErrorCode enumeration


## -description

The 
   <b>RDC_ErrorCode</b> enumeration type
   defines the set of RDC-specific error codes.

## -enum-fields

### -field RDC_NoError:0

The operation was completed successfully.

### -field RDC_HeaderVersionNewer

The data header is incompatible with this library.

### -field RDC_HeaderVersionOlder

The data header is incompatible with this library.

### -field RDC_HeaderMissingOrCorrupt

The data header is missing or corrupt.

### -field RDC_HeaderWrongType

The data header format is incorrect.

### -field RDC_DataMissingOrCorrupt

The end of data was reached before all data expected was read.

### -field RDC_DataTooManyRecords

Additional data was found past where the end of data was expected.

### -field RDC_FileChecksumMismatch

The final file checksum doesn't match.

### -field RDC_ApplicationError

An application callback function returned failure.

### -field RDC_Aborted

The operation was aborted.

### -field RDC_Win32Error

The failure of the function is not RDC-specific and the <b>HRESULT</b> returned by 
      the function contains the specific error code.

## -see-also

<a href="/previous-versions/windows/desktop/rdc/remote-differential-compression-enumerations">Remote Differential Compression Enumerations</a>
