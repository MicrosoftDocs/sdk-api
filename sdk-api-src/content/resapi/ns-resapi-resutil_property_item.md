---
UID: NS:resapi.RESUTIL_PROPERTY_ITEM
title: RESUTIL_PROPERTY_ITEM
author: windows-sdk-content
description: Contains information about a cluster object property. An array of RESUTIL_PROPERTY_ITEM structures forms a property table which can be used in property operations.
old-location: mscs\resutil_property_item.htm
old-project: MsCS
ms.assetid: f65ee50f-59f7-44db-ad69-b29b3e693c7e
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PRESUTIL_PROPERTY_ITEM, PRESUTIL_PROPERTY_ITEM, PRESUTIL_PROPERTY_ITEM structure pointer [Failover Cluster], RESUTIL_PROPERTY_ITEM, RESUTIL_PROPERTY_ITEM structure [Failover Cluster], RESUTIL_PROPITEM_READ_ONLY, RESUTIL_PROPITEM_REQUIRED, RESUTIL_PROPITEM_SIGNED, _wolf_resutil_property_item, mscs.resutil_property_item, resapi/PRESUTIL_PROPERTY_ITEM, resapi/RESUTIL_PROPERTY_ITEM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RESUTIL_PROPERTY_ITEM, *PRESUTIL_PROPERTY_ITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ResApi.h
api_name:
-	RESUTIL_PROPERTY_ITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RESUTIL_PROPERTY_ITEM structure


## -description


Contains 
    information about a cluster object property. An array of 
    <b>RESUTIL_PROPERTY_ITEM</b> structures forms a 
    <a href="https://msdn.microsoft.com/48591d73-606b-42b4-9711-4f7a84e9e971">property table</a> which can be used in property operations.


## -struct-fields




### -field Name

The name of the property.


### -field KeyName

Optional name of the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a> subkey for 
      the property. This parameter can be <b>NULL</b>.


### -field Format

Describes the format of the property such as <b>CLUSPROP_FORMAT_BINARY</b> or 
      <b>CLUSPROP_FORMAT_DWORD</b>. For a list of valid format values, see the 
      <b>wFormat</b> member of 
      <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DefaultPtr

 


### -field DUMMYUNIONNAME.Default

 


### -field DUMMYUNIONNAME.lpDefault

 


### -field DUMMYUNIONNAME.LargeIntData

 


### -field DUMMYUNIONNAME.ULargeIntData

 


### -field DUMMYUNIONNAME.FileTimeData

 


### -field Minimum

Minimum data value for the property. For data values with the 
      <b>CLUSPROP_FORMAT_BINARY</b> and <b>CLUSPROP_FORMAT_MULTI_SZ</b> 
      formats, the <b>Minimum</b> member contains the byte size of the default data value 
      specified by <b>Default</b>.


### -field Maximum

Maximum data value for the property.


### -field Flags

Bitmask that describes the property.



#### RESUTIL_PROPITEM_READ_ONLY (0x00000001)

The property is <a href="https://msdn.microsoft.com/7df0981b-7253-40c1-9a5d-44cfc4cdf13b">read-only</a>.



#### RESUTIL_PROPITEM_REQUIRED (0x00000002)

The property is required.



#### RESUTIL_PROPITEM_SIGNED (0x00000004)

Flags a numeric property as a signed value.


### -field Offset

Byte offset to the actual property data. The data is stored in a buffer known as a parameter block.


#### - ( unnamed union )

The default value of the property in one of the following forms.



#### DefaultPtr

Pointer to a <b>DWORD</b> default value.



#### Default

A <b>DWORD</b> default value.



#### lpDefault

Void pointer to a buffer containing the default value.



#### LargeIntData

Pointer to a <a href="https://msdn.microsoft.com/2498a771-f430-4faa-81c8-78d56905d18b">RESUTIL_LARGEINT_DATA</a> 
       structure describing the maximum, minimum, and default values for a signed large integer.



#### ULargeIntData

Pointer to a <a href="https://msdn.microsoft.com/44b937dc-e2f1-4c2d-9689-35b772103b8d">RESUTIL_ULARGEINT_DATA</a> 
       structure describing the maximum, minimum, and default values for an unsigned large integer. The default value 
       must be consistent with the format specified by the <b>Format</b> member.



#### FileTimeData

Pointer to a <a href="https://msdn.microsoft.com/47009cac-fcfe-43f5-9676-4e5db863c909">RESUTIL_FILETIME_DATA</a> 
       structure describing the file data and time data.


## -remarks



For more information about building parameter blocks and property tables, see 
    <a href="https://msdn.microsoft.com/f8f0297a-c050-41b9-a52f-a0265a18b87a">Using Lists and Tables</a>.


#### Examples

See <a href="https://msdn.microsoft.com/f8f0297a-c050-41b9-a52f-a0265a18b87a">Using Lists and Tables</a> and 
     <a href="https://msdn.microsoft.com/9efe1457-72ab-4e9a-9d92-128e206b0fb3">Building with CLUSPROP_BUFFER_HELPER</a>, 
     and <a href="https://msdn.microsoft.com/20b150b4-293f-408b-888e-bac2b2fa4fb8">Defining Structures and Constants</a> in 
     <a href="https://msdn.microsoft.com/400862c3-73c4-443d-bc60-1c1b6b34534f">Implementing Resource DLLs</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>
 

 

