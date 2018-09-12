---
UID: NS:clusapi.CLUSPROP_SYNTAX
title: CLUSPROP_SYNTAX
author: windows-sdk-content
description: Describes the format and type of a data value. It is used as the Syntax member of the CLUSPROP_VALUE structure.
old-location: mscs\clusprop_syntax.htm
tech.root: mscs
ms.assetid: 23353e11-63bb-4d3b-90fb-e2a5544e0d09
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCLUSPROP_SYNTAX, CLUSPROP_FORMAT_BINARY, CLUSPROP_FORMAT_DWORD, CLUSPROP_FORMAT_EXPANDED_SZ, CLUSPROP_FORMAT_EXPAND_SZ, CLUSPROP_FORMAT_FILETIME, CLUSPROP_FORMAT_LARGE_INTEGER, CLUSPROP_FORMAT_LONG, CLUSPROP_FORMAT_MULTI_SZ, CLUSPROP_FORMAT_SECURITY_DESCRIPTOR, CLUSPROP_FORMAT_SZ, CLUSPROP_FORMAT_ULARGE_INTEGER, CLUSPROP_FORMAT_UNKNOWN, CLUSPROP_FORMAT_USER, CLUSPROP_FORMAT_WORD, CLUSPROP_SYNTAX, CLUSPROP_SYNTAX union [Failover Cluster], CLUSPROP_TYPE_DISK_GUID, CLUSPROP_TYPE_DISK_NUMBER, CLUSPROP_TYPE_DISK_SERIALNUMBER, CLUSPROP_TYPE_DISK_SIZE, CLUSPROP_TYPE_ENDMARK, CLUSPROP_TYPE_LIST_VALUE, CLUSPROP_TYPE_NAME, CLUSPROP_TYPE_PARTITION_INFO, CLUSPROP_TYPE_PARTITION_INFO_EX, CLUSPROP_TYPE_RESCLASS, CLUSPROP_TYPE_SCSI_ADDRESS, CLUSPROP_TYPE_SIGNATURE, CLUSPROP_TYPE_UNKNOWN, CLUSPROP_TYPE_USER, PCLUSPROP_SYNTAX, PCLUSPROP_SYNTAX union pointer [Failover Cluster], _wolf_clusprop_syntax, clusapi/CLUSPROP_SYNTAX, clusapi/PCLUSPROP_SYNTAX, mscs.clusprop_syntax"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_SYNTAX
product: Windows
targetos: Windows
req.typenames: CLUSPROP_SYNTAX, *PCLUSPROP_SYNTAX
req.redist: 
---

# CLUSPROP_SYNTAX structure


## -description


Describes the format and type of a data value. It is used as the <b>Syntax</b> member of the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a> structure.


## -struct-fields




### -field dw

A DWORD that describes the format and type of the data value. The 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309159(v=VS.85).aspx">CLUSTER_PROPERTY_SYNTAX</a> enumeration defines the 
       possible values.


### -field DUMMYSTRUCTNAME


### -field DUMMYSTRUCTNAME.wFormat

Numeric value describing only the format of the data value. ClusAPI.h defines the following values, 
        enumerated in the <a href="https://msdn.microsoft.com/en-us/library/Bb309158(v=VS.85).aspx">CLUSTER_PROPERTY_FORMAT</a> 
        enumeration.



##### wFormat.CLUSPROP_FORMAT_BINARY (1)

Data is a binary value.



##### wFormat.CLUSPROP_FORMAT_DWORD (2)

Data is a <b>DWORD</b> value.



##### wFormat.CLUSPROP_FORMAT_EXPAND_SZ (4)

Data is a null-terminated Unicode string with unexpanded references to environment variables.



##### wFormat.CLUSPROP_FORMAT_EXPANDED_SZ (8)

Data is a null-terminated Unicode string with expanded references to environment variables.



##### wFormat.CLUSPROP_FORMAT_FILETIME (12 (0xC))

Data is a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>.



##### wFormat.CLUSPROP_FORMAT_LARGE_INTEGER (10 (0xA))

Data is a signed large integer.



##### wFormat.CLUSPROP_FORMAT_LONG (7)

Data is an signed <b>LONG</b> value.



##### wFormat.CLUSPROP_FORMAT_MULTI_SZ (5)

Data is an array of null-terminated Unicode strings.



##### wFormat.CLUSPROP_FORMAT_SECURITY_DESCRIPTOR (9)

Data is a <a href="https://msdn.microsoft.com/en-us/library/Aa379561(v=VS.85).aspx">SECURITY_DESCRIPTOR</a> in 
          <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">self-relative</a> 
          format. For more information about self-relative security descriptors, see 
          <a href="https://msdn.microsoft.com/en-us/library/Aa374807(v=VS.85).aspx">Absolute and Self-Relative Security Descriptors</a>.



##### wFormat.CLUSPROP_FORMAT_SZ (3)

Data is a null-terminated Unicode string.



##### wFormat.CLUSPROP_FORMAT_ULARGE_INTEGER (6)

Data is an unsigned large integer.



##### wFormat.CLUSPROP_FORMAT_UNKNOWN (0)

Data is in an unknown format.



##### wFormat.CLUSPROP_FORMAT_USER (32768 (0x8000))

Data is in a user-defined format.



##### wFormat.CLUSPROP_FORMAT_WORD (11 (0xB))

Data is a <b>WORD</b> value.


### -field DUMMYSTRUCTNAME.wType

Numeric value that describes only the type of the data value. The 
        <a href="https://msdn.microsoft.com/en-us/library/Bb309160(v=VS.85).aspx">CLUSTER_PROPERTY_TYPE</a> enumeration defines the 
        possible values.



##### wType.CLUSPROP_TYPE_DISK_NUMBER (7)

Describes the number value of a disk resource. A disk number value is represented by a 
          <a href="https://msdn.microsoft.com/en-us/library/Aa368373(v=VS.85).aspx">CLUSPROP_DISK_NUMBER</a> 
          structure.



##### wType.CLUSPROP_TYPE_DISK_SERIALNUMBER (10 (0xA))

Describes the serial number of a disk resource.



##### wType.CLUSPROP_TYPE_DISK_GUID (11 (0xB))

Describes the <b>GUID</b> of a disk resource.



##### wType.CLUSPROP_TYPE_DISK_SIZE (12 (0xC))

Describes the total size of the disk.



##### wType.CLUSPROP_TYPE_ENDMARK (0)

Designates the data value as the last entry in a property or value list.



##### wType.CLUSPROP_TYPE_LIST_VALUE (1)

Describes a data value in a property list. For example, in the property list passed to a 
          <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code function</a> for a property 
          validation operation, <b>CLUSPROP_TYPE_LIST_VALUE</b> is the required type to be 
          included with each property value.



##### wType.CLUSPROP_TYPE_NAME (4)

Describes a data value used as a name, such as a property name. A name value is represented by a 
          <a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a> 
          structure.



##### wType.CLUSPROP_TYPE_PARTITION_INFO (8)

Describes a collection of information about a disk resource, such as its device name and volume label. 
          Partition data is represented by a 
          <a href="https://msdn.microsoft.com/en-us/library/Aa368381(v=VS.85).aspx">CLUSPROP_PARTITION_INFO</a> 
          structure.



##### wType.CLUSPROP_TYPE_PARTITION_INFO_EX (13 (0xD))

Describes a collection of information about a disk resource, such as its device name and volume label. 
          Partition data is represented by a 
          <a href="https://msdn.microsoft.com/en-us/library/Bb309113(v=VS.85).aspx">CLUSPROP_PARTITION_INFO_EX</a> 
          structure.



##### wType.CLUSPROP_TYPE_RESCLASS (2)

Describes resource class information. A resource class value is described with a 
          <a href="https://msdn.microsoft.com/en-us/library/Aa368385(v=VS.85).aspx">CLUSPROP_RESOURCE_CLASS</a> 
          structure. Resource classes are returned when an application calls 
          <a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a> or 
          <a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a> with one 
          of the following control codes.


<a href="https://msdn.microsoft.com/en-us/library/Aa367467(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367504(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367647(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>




##### wType.CLUSPROP_TYPE_SCSI_ADDRESS (6)

Describes an <a href="https://msdn.microsoft.com/en-us/library/Aa370485(v=VS.85).aspx">Address</a> 
          property for an <a href="https://msdn.microsoft.com/en-us/library/Aa370484(v=VS.85).aspx">IP Address</a> resource. A SCSI 
          address value is represented by a 
          <a href="https://msdn.microsoft.com/en-us/library/Aa368387(v=VS.85).aspx">CLUSPROP_SCSI_ADDRESS</a> 
          structure.



##### wType.CLUSPROP_TYPE_SIGNATURE (5)

Describes a <a href="https://msdn.microsoft.com/en-us/library/Aa371795(v=VS.85).aspx">Signature</a> property for a 
          disk resource. A signature value is represented by a 
          <a href="https://msdn.microsoft.com/38400cce-d84a-4439-9dab-20102c1580ff">CLUSPROP_DISK_SIGNATURE</a> 
          structure.



##### wType.CLUSPROP_TYPE_UNKNOWN (-1)

The type is unknown.



##### wType.CLUSPROP_TYPE_USER (32768 (0x8000))

Describes the beginning of the range for users to define their own types. Associate this type with 
          user-defined private properties.


## -remarks



To parse data that is returned from a 
     <a href="https://msdn.microsoft.com/en-us/library/Aa369310(v=VS.85).aspx">control code function</a>, use the 
     <b>wFormat</b> member of this structure if the <b>wType</b> member 
     defines a type that the application cannot understand.


#### Examples

See <a href="https://msdn.microsoft.com/en-us/library/Aa369328(v=VS.85).aspx">Creating Physical Disk Resources</a> 
     and 
     <a href="https://msdn.microsoft.com/en-us/library/Aa367188(v=VS.85).aspx">Building with CLUSPROP_BUFFER_HELPER</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370485(v=VS.85).aspx">Address</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367467(v=VS.85).aspx">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367504(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa367647(v=VS.85).aspx">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368368(v=VS.85).aspx">CLUSPROP_BINARY</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368373(v=VS.85).aspx">CLUSPROP_DISK_NUMBER</a>



<a href="https://msdn.microsoft.com/38400cce-d84a-4439-9dab-20102c1580ff">CLUSPROP_DISK_SIGNATURE</a>



<a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309110(v=VS.85).aspx">CLUSPROP_FILETIME</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368379(v=VS.85).aspx">CLUSPROP_LONG</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368380(v=VS.85).aspx">CLUSPROP_MULTI_SZ</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368381(v=VS.85).aspx">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309113(v=VS.85).aspx">CLUSPROP_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368385(v=VS.85).aspx">CLUSPROP_RESOURCE_CLASS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368387(v=VS.85).aspx">CLUSPROP_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa368389(v=VS.85).aspx">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>



<b>CLUSPROP_ULARGE_INTEGER</b>



<a href="https://msdn.microsoft.com/en-us/library/Aa368393(v=VS.85).aspx">CLUSPROP_VALUE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309158(v=VS.85).aspx">CLUSTER_PROPERTY_FORMAT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309159(v=VS.85).aspx">CLUSTER_PROPERTY_SYNTAX</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309160(v=VS.85).aspx">CLUSTER_PROPERTY_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369016(v=VS.85).aspx">ClusterResourceControl</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369036(v=VS.85).aspx">ClusterResourceTypeControl</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>



<a href="https://msdn.microsoft.com/61a4a2bc-e18f-4fac-82f0-8d5ef58e8d70">Name (property for resources)</a>



<a href="https://msdn.microsoft.com/a16f245e-6191-428a-acfa-b70294633ecb">NodeName</a>
 

 

