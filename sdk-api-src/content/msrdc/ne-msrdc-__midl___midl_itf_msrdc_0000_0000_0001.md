---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# __MIDL___MIDL_itf_msrdc_0000_0000_0001 enumeration


## -description


The 
   <b>RDC_ErrorCode</b> enumeration type
   defines the set of RDC-specific error codes.


## -enum-fields




### -field RDC_NoError

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




<a href="https://msdn.microsoft.com/83e11884-d174-4dae-99fa-321a2b47122c">Remote Differential Compression Enumerations</a>
 

 

