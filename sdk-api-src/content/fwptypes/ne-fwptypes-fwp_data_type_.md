---
UID: NE:fwptypes.FWP_DATA_TYPE_
title: FWP_DATA_TYPE_
author: windows-sdk-content
description: The FWP_DATA_TYPE enumeration type specifies a type of data.
old-location: netvista\fwp_data_type.htm
tech.root: NetVista
ms.assetid: 7632d9be-dd16-40d2-b7b4-2d4efb6aaa99
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_BYTE_ARRAY16_TYPE, FWP_BYTE_ARRAY6_TYPE, FWP_BYTE_BLOB_TYPE, FWP_DATA_TYPE, FWP_DATA_TYPE enumeration [Network Drivers Starting with Windows Vista], FWP_DATA_TYPE_, FWP_DATA_TYPE_MAX, FWP_DOUBLE, FWP_EMPTY, FWP_FLOAT, FWP_INT16, FWP_INT32, FWP_INT64, FWP_INT8, FWP_RANGE_TYPE, FWP_SECURITY_DESCRIPTOR_TYPE, FWP_SID, FWP_SINGLE_DATA_TYPE_MAX, FWP_TOKEN_ACCESS_INFORMATION_TYPE, FWP_TOKEN_INFORMATION_TYPE, FWP_UINT16, FWP_UINT32, FWP_UINT64, FWP_UINT8, FWP_UNICODE_STRING_TYPE, FWP_V4_ADDR_MASK, FWP_V6_ADDR_MASK, fwptypes/FWP_BYTE_ARRAY16_TYPE, fwptypes/FWP_BYTE_ARRAY6_TYPE, fwptypes/FWP_BYTE_BLOB_TYPE, fwptypes/FWP_DATA_TYPE, fwptypes/FWP_DATA_TYPE_MAX, fwptypes/FWP_DOUBLE, fwptypes/FWP_EMPTY, fwptypes/FWP_FLOAT, fwptypes/FWP_INT16, fwptypes/FWP_INT32, fwptypes/FWP_INT64, fwptypes/FWP_INT8, fwptypes/FWP_RANGE_TYPE, fwptypes/FWP_SECURITY_DESCRIPTOR_TYPE, fwptypes/FWP_SID, fwptypes/FWP_SINGLE_DATA_TYPE_MAX, fwptypes/FWP_TOKEN_ACCESS_INFORMATION_TYPE, fwptypes/FWP_TOKEN_INFORMATION_TYPE, fwptypes/FWP_UINT16, fwptypes/FWP_UINT32, fwptypes/FWP_UINT64, fwptypes/FWP_UINT8, fwptypes/FWP_UNICODE_STRING_TYPE, fwptypes/FWP_V4_ADDR_MASK, fwptypes/FWP_V6_ADDR_MASK, netvista.fwp_data_type, wfp_ref_4_enum_68613d11-4251-4e6f-bf0c-2b5169e78a5e.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows Vista.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_DATA_TYPE
product: Windows
targetos: Windows
req.typenames: FWP_DATA_TYPE
req.redist: 
---

# FWP_DATA_TYPE_ enumeration


## -description


The FWP_DATA_TYPE enumeration type specifies a type of data.


## -enum-fields




### -field FWP_EMPTY

Indicates no data.


### -field FWP_UINT8

Indicates an unsigned 8-bit integer value.


### -field FWP_UINT16

Indicates an unsigned 16-bit integer value.


### -field FWP_UINT32

Indicates an unsigned 32-bit integer value.


### -field FWP_UINT64

Indicates a pointer to an unsigned 64-bit integer value.


### -field FWP_INT8

Indicates a signed 8-bit integer value.


### -field FWP_INT16

Indicates a signed 16-bit integer value.


### -field FWP_INT32

Indicates a signed 32-bit integer value.


### -field FWP_INT64

Indicates a pointer to a signed 64-bit integer value.


### -field FWP_FLOAT

Indicates a single-precision floatin-point value.


### -field FWP_DOUBLE

Indicates a pointer to a double-precision floating-point value.


### -field FWP_BYTE_ARRAY16_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/fcccd92d-6f00-4ab4-b730-4ddacdb900ff">FWP_BYTE_ARRAY16</a> structure.


### -field FWP_BYTE_BLOB_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure.


### -field FWP_SID

Indicates a pointer to a security identifier (SID) structure. For more information about the SID
     structure, see the description for the SID structure in the Microsoft Windows SDK documentation.


### -field FWP_SECURITY_DESCRIPTOR_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure in which the 
     <b>Data</b> member points to a 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=90125">SECURITY_DESCRIPTOR</a> structure that
     specifies security information.


### -field FWP_TOKEN_INFORMATION_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/e30a5441-3f36-4da9-a066-9937a484de84">FWP_TOKEN_INFORMATION</a> structure that
     describes token information.


### -field FWP_TOKEN_ACCESS_INFORMATION_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure in which the 
     <b>Data</b> member points to a 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=108853">TOKEN_ACCESS_INFORMATION</a> structure
     that specifies token access information.


### -field FWP_UNICODE_STRING_TYPE

Indicates a pointer to a null-terminated string of Unicode characters.


### -field FWP_BYTE_ARRAY6_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/395b5c1c-988b-4d85-9b31-c1f84e02a90c">FWP_BYTE_ARRAY6</a> structure.


### -field FWP_BITMAP_INDEX_TYPE


### -field FWP_BITMAP_ARRAY64_TYPE


### -field FWP_SINGLE_DATA_TYPE_MAX

A maximum value for testing purposes.


### -field FWP_V4_ADDR_MASK

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/3beefa33-1331-4a76-b705-6060a00901f2">FWP_V4_ADDR_AND_MASK</a> structure.


### -field FWP_V6_ADDR_MASK

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/63fb08f1-b333-40de-97d9-d98792256954">FWP_V6_ADDR_AND_MASK</a> structure.


### -field FWP_RANGE_TYPE

Indicates a pointer to an 
     <a href="https://msdn.microsoft.com/66410df3-0856-4b2e-a586-1a75b97e0047">FWP_RANGE0</a> structure.


### -field FWP_DATA_TYPE_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


## -remarks



The 
    <a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a> and 
    <a href="https://msdn.microsoft.com/8d0aad8c-b224-4066-a10a-7c11ca60a78c">FWP_CONDITION_VALUE0</a> structures each
    contain a member of type FWP_DATA_TYPE that specifies the type of data that is contained within the
    structure.




## -see-also




<a href="https://msdn.microsoft.com/fcccd92d-6f00-4ab4-b730-4ddacdb900ff">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/8d0aad8c-b224-4066-a10a-7c11ca60a78c">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/66410df3-0856-4b2e-a586-1a75b97e0047">FWP_RANGE0</a>



<a href="https://msdn.microsoft.com/e30a5441-3f36-4da9-a066-9937a484de84">FWP_TOKEN_INFORMATION</a>



<a href="https://msdn.microsoft.com/3beefa33-1331-4a76-b705-6060a00901f2">FWP_V4_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/63fb08f1-b333-40de-97d9-d98792256954">FWP_V6_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a>
 

 

