---
UID: NS:fwptypes.FWP_CONDITION_VALUE0_
title: FWP_CONDITION_VALUE0_
author: windows-sdk-content
description: The FWP_CONDITION_VALUE0 structure defines a condition value that is used by the filter engine when testing a data field against a filtering condition.Note  FWP_CONDITION_VALUE0 is a specific version of FWP_CONDITION_VALUE.
old-location: netvista\fwp_condition_value0.htm
tech.root: NetVista
ms.assetid: 8d0aad8c-b224-4066-a10a-7c11ca60a78c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_CONDITION_VALUE0, FWP_CONDITION_VALUE0 structure [Network Drivers Starting with Windows Vista], FWP_CONDITION_VALUE0_, fwptypes/FWP_CONDITION_VALUE0, netvista.fwp_condition_value0, wfp_ref_3_struct_1_top_fwp_A-Z_8ed44bab-c9e7-468c-9028-61888d24b807.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
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
 - FWP_CONDITION_VALUE0
product: Windows
targetos: Windows
req.typenames: FWP_CONDITION_VALUE0
req.redist: 
---

# FWP_CONDITION_VALUE0_ structure


## -description


The <b>FWP_CONDITION_VALUE0</b> structure defines a condition value that is used by the filter engine when
  testing a data field against a filtering condition.
<div class="alert"><b>Note</b>  <b>FWP_CONDITION_VALUE0</b> is a specific version of <b>FWP_CONDITION_VALUE</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field type

The type of data that is described by the structure. For the possible values for this data member,
     see 
     <a href="https://msdn.microsoft.com/7632d9be-dd16-40d2-b7b4-2d4efb6aaa99">FWP_DATA_TYPE</a>.


### -field uint8

An unsigned 8-bit value. Used when the 
      <b>Type</b> member is set to FWP_UINT8.


### -field uint16

An unsigned 16-bit value. Used when the 
      <b>Type</b> member is set to FWP_UINT16.


### -field uint32

An unsigned 32-bit value. Used when the 
      <b>Type</b> member is set to FWP_UINT32.


### -field uint64

A pointer to an unsigned 64-bit value. Used when the 
      <b>Type</b> member is set to FWP_UINT64.


### -field int8

A signed 8-bit value. Used when the 
      <b>Type</b> member is set to FWP_INT8.


### -field int16

A signed 16-bit value. Used when the 
      <b>Type</b> member is set to FWP_INT16.


### -field int32

A signed 32-bit value. Used when the 
      <b>Type</b> member is set to FWP_INT32.


### -field int64

A pointer to a signed 64-bit value. Used when the 
      <b>Type</b> member is set to FWP_INT64.


### -field float32

A single-precision floating point value. Used when the 
      <b>Type</b> member is set to FWP_FLOAT.


### -field double64

A pointer to a double-precision floating-point value. Used when the 
      <b>Type</b> member is set to FWP_DOUBLE.


### -field byteArray16

A pointer to an 
      <a href="https://msdn.microsoft.com/fcccd92d-6f00-4ab4-b730-4ddacdb900ff">FWP_BYTE_ARRAY16</a> structure. Used when the
      
      <b>Type</b> member is set to FWP_BYTE_ARRAY16_TYPE.


### -field byteBlob

A pointer to an 
      <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure. Used when the 
      <b>Type</b> member is set to FWP_BYTE_BLOB_TYPE.


### -field sid

A pointer to a security identifier (SID) structure. Used when the 
      <b>Type</b> member is set to FWP_SID. For more information about the SID structure, see the description
      for the SID structure in the Microsoft Windows SDK documentation.


### -field sd

A pointer to an 
      <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure that describes a
      security descriptor. Used when the 
      <b>Type</b> member is set to FWP_SECURITY_DESCRIPTOR_TYPE.


### -field tokenInformation

A pointer to an 
      <a href="https://msdn.microsoft.com/e30a5441-3f36-4da9-a066-9937a484de84">FWP_TOKEN_INFORMATION</a> structure.
      Used when the 
      <b>Type</b> member is set to FWP_TOKEN_INFORMATION_TYPE.


### -field tokenAccessInformation

A pointer to an 
      <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure that describes token
      access information. Used when the 
      <b>Type</b> member is set to FWP_TOKEN_ACCESS_INFORMATION_TYPE.


### -field unicodeString

A pointer to a null-terminated string of Unicode characters. Used when the 
      <b>Type</b> member is set to FWP_UNICODE_STRING_TYPE.


### -field byteArray6

A pointer to an 
      <a href="https://msdn.microsoft.com/395b5c1c-988b-4d85-9b31-c1f84e02a90c">FWP_BYTE_ARRAY6</a> structure. Used when the 
      <b>Type</b> member is set to FWP_BYTE_ARRAY6_TYPE.


### -field bitmapArray64

 


### -field v4AddrMask

A pointer to an 
      <a href="https://msdn.microsoft.com/3beefa33-1331-4a76-b705-6060a00901f2">FWP_V4_ADDR_AND_MASK</a> structure. Used
      when the 
      <b>Type</b> member is set to FWP_V4_ADDR_MASK.


### -field v6AddrMask

A pointer to an 
      <a href="https://msdn.microsoft.com/63fb08f1-b333-40de-97d9-d98792256954">FWP_V6_ADDR_AND_MASK</a> structure. Used
      when the 
      <b>Type</b> member is set to FWP_V6_ADDR_MASK.


### -field rangeValue

A pointer to an 
      <a href="https://msdn.microsoft.com/66410df3-0856-4b2e-a586-1a75b97e0047">FWP_RANGE0</a> structure. Used when the 
      <b>Type</b> member is set to FWP_RANGE_TYPE.


## -remarks



An FWP_CONDITION_VALUE0 structure is contained within an 
    <a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a> structure and
    specifies the condition value for the filtering condition.




## -see-also




<a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a>



<a href="https://msdn.microsoft.com/fcccd92d-6f00-4ab4-b730-4ddacdb900ff">FWP_BYTE_ARRAY16</a>



<a href="https://msdn.microsoft.com/395b5c1c-988b-4d85-9b31-c1f84e02a90c">FWP_BYTE_ARRAY6</a>



<a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/7632d9be-dd16-40d2-b7b4-2d4efb6aaa99">FWP_DATA_TYPE</a>



<a href="https://msdn.microsoft.com/66410df3-0856-4b2e-a586-1a75b97e0047">FWP_RANGE0</a>



<a href="https://msdn.microsoft.com/e30a5441-3f36-4da9-a066-9937a484de84">FWP_TOKEN_INFORMATION</a>



<a href="https://msdn.microsoft.com/3beefa33-1331-4a76-b705-6060a00901f2">FWP_V4_ADDR_AND_MASK</a>



<a href="https://msdn.microsoft.com/63fb08f1-b333-40de-97d9-d98792256954">FWP_V6_ADDR_AND_MASK</a>
 

 

