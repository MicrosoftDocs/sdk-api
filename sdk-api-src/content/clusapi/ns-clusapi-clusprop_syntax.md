---
UID: NS:clusapi.CLUSPROP_SYNTAX
title: CLUSPROP_SYNTAX (clusapi.h)
description: Describes the format and type of a data value. It is used as the Syntax member of the CLUSPROP_VALUE structure.
helpviewer_keywords: ["*PCLUSPROP_SYNTAX","CLUSPROP_FORMAT_BINARY","CLUSPROP_FORMAT_DWORD","CLUSPROP_FORMAT_EXPANDED_SZ","CLUSPROP_FORMAT_EXPAND_SZ","CLUSPROP_FORMAT_FILETIME","CLUSPROP_FORMAT_LARGE_INTEGER","CLUSPROP_FORMAT_LONG","CLUSPROP_FORMAT_MULTI_SZ","CLUSPROP_FORMAT_SECURITY_DESCRIPTOR","CLUSPROP_FORMAT_SZ","CLUSPROP_FORMAT_ULARGE_INTEGER","CLUSPROP_FORMAT_UNKNOWN","CLUSPROP_FORMAT_USER","CLUSPROP_FORMAT_WORD","CLUSPROP_SYNTAX","CLUSPROP_SYNTAX union [Failover Cluster]","CLUSPROP_TYPE_DISK_GUID","CLUSPROP_TYPE_DISK_NUMBER","CLUSPROP_TYPE_DISK_SERIALNUMBER","CLUSPROP_TYPE_DISK_SIZE","CLUSPROP_TYPE_ENDMARK","CLUSPROP_TYPE_LIST_VALUE","CLUSPROP_TYPE_NAME","CLUSPROP_TYPE_PARTITION_INFO","CLUSPROP_TYPE_PARTITION_INFO_EX","CLUSPROP_TYPE_RESCLASS","CLUSPROP_TYPE_SCSI_ADDRESS","CLUSPROP_TYPE_SIGNATURE","CLUSPROP_TYPE_UNKNOWN","CLUSPROP_TYPE_USER","PCLUSPROP_SYNTAX","PCLUSPROP_SYNTAX union pointer [Failover Cluster]","_wolf_clusprop_syntax","clusapi/CLUSPROP_SYNTAX","clusapi/PCLUSPROP_SYNTAX","mscs.clusprop_syntax"]
old-location: mscs\clusprop_syntax.htm
tech.root: MsCS
ms.assetid: 23353e11-63bb-4d3b-90fb-e2a5544e0d09
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_SYNTAX, CLUSPROP_FORMAT_BINARY, CLUSPROP_FORMAT_DWORD, CLUSPROP_FORMAT_EXPANDED_SZ, CLUSPROP_FORMAT_EXPAND_SZ, CLUSPROP_FORMAT_FILETIME, CLUSPROP_FORMAT_LARGE_INTEGER, CLUSPROP_FORMAT_LONG, CLUSPROP_FORMAT_MULTI_SZ, CLUSPROP_FORMAT_SECURITY_DESCRIPTOR, CLUSPROP_FORMAT_SZ, CLUSPROP_FORMAT_ULARGE_INTEGER, CLUSPROP_FORMAT_UNKNOWN, CLUSPROP_FORMAT_USER, CLUSPROP_FORMAT_WORD, CLUSPROP_SYNTAX, CLUSPROP_SYNTAX union [Failover Cluster], CLUSPROP_TYPE_DISK_GUID, CLUSPROP_TYPE_DISK_NUMBER, CLUSPROP_TYPE_DISK_SERIALNUMBER, CLUSPROP_TYPE_DISK_SIZE, CLUSPROP_TYPE_ENDMARK, CLUSPROP_TYPE_LIST_VALUE, CLUSPROP_TYPE_NAME, CLUSPROP_TYPE_PARTITION_INFO, CLUSPROP_TYPE_PARTITION_INFO_EX, CLUSPROP_TYPE_RESCLASS, CLUSPROP_TYPE_SCSI_ADDRESS, CLUSPROP_TYPE_SIGNATURE, CLUSPROP_TYPE_UNKNOWN, CLUSPROP_TYPE_USER, PCLUSPROP_SYNTAX, PCLUSPROP_SYNTAX union pointer [Failover Cluster], _wolf_clusprop_syntax, clusapi/CLUSPROP_SYNTAX, clusapi/PCLUSPROP_SYNTAX, mscs.clusprop_syntax'
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
targetos: Windows
req.typenames: CLUSPROP_SYNTAX, *PCLUSPROP_SYNTAX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_SYNTAX
 - clusapi/CLUSPROP_SYNTAX
 - PCLUSPROP_SYNTAX
 - clusapi/PCLUSPROP_SYNTAX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSPROP_SYNTAX
---

# CLUSPROP_SYNTAX structure


## -description

Describes the format and type of a data value. It is used as the <b>Syntax</b> member of the 
    <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure.

## -struct-fields

### -field dw

A DWORD that describes the format and type of the data value. The 
       <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_syntax">CLUSTER_PROPERTY_SYNTAX</a> enumeration defines the 
       possible values.

### -field DUMMYSTRUCTNAME

### -field DUMMYSTRUCTNAME.wFormat

Numeric value describing only the format of the data value. ClusAPI.h defines the following values, 
        enumerated in the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_format">CLUSTER_PROPERTY_FORMAT</a> 
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

Data is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>.



##### wFormat.CLUSPROP_FORMAT_LARGE_INTEGER (10 (0xA))

Data is a signed large integer.



##### wFormat.CLUSPROP_FORMAT_LONG (7)

Data is a signed <b>LONG</b> value.



##### wFormat.CLUSPROP_FORMAT_MULTI_SZ (5)

Data is an array of null-terminated Unicode strings.



##### wFormat.CLUSPROP_FORMAT_SECURITY_DESCRIPTOR (9)

Data is a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> in 
          <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> 
          format. For more information about self-relative security descriptors, see 
          <a href="/windows/desktop/SecAuthZ/absolute-and-self-relative-security-descriptors">Absolute and Self-Relative Security Descriptors</a>.



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
        <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_type">CLUSTER_PROPERTY_TYPE</a> enumeration defines the 
        possible values.



##### wType.CLUSPROP_TYPE_DISK_NUMBER (7)

Describes the number value of a disk resource. A disk number value is represented by a 
          <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_dword">CLUSPROP_DISK_NUMBER</a> 
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
          <a href="/previous-versions/windows/desktop/mscs/control-code-functions">control code function</a> for a property 
          validation operation, <b>CLUSPROP_TYPE_LIST_VALUE</b> is the required type to be 
          included with each property value.



##### wType.CLUSPROP_TYPE_NAME (4)

Describes a data value used as a name, such as a property name. A name value is represented by a 
          <a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a> 
          structure.



##### wType.CLUSPROP_TYPE_PARTITION_INFO (8)

Describes a collection of information about a disk resource, such as its device name and volume label. 
          Partition data is represented by a 
          <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a> 
          structure.



##### wType.CLUSPROP_TYPE_PARTITION_INFO_EX (13 (0xD))

Describes a collection of information about a disk resource, such as its device name and volume label. 
          Partition data is represented by a 
          <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex">CLUSPROP_PARTITION_INFO_EX</a> 
          structure.



##### wType.CLUSPROP_TYPE_RESCLASS (2)

Describes resource class information. A resource class value is described with a 
          <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class">CLUSPROP_RESOURCE_CLASS</a> 
          structure. Resource classes are returned when an application calls 
          <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> or 
          <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a> with one 
          of the following control codes.


<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-class-info">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-required-dependencies">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>




##### wType.CLUSPROP_TYPE_SCSI_ADDRESS (6)

Describes an <a href="/previous-versions/windows/desktop/mscs/ip-addresses-address">Address</a> 
          property for an <a href="/previous-versions/windows/desktop/mscs/ip-address">IP Address</a> resource. A SCSI 
          address value is represented by a 
          <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a> 
          structure.



##### wType.CLUSPROP_TYPE_SIGNATURE (5)

Describes a <a href="/previous-versions/windows/desktop/mscs/physical-disks-signature">Signature</a> property for a 
          disk resource. A signature value is represented by a 
          <a href="/previous-versions/windows/desktop/legacy/aa368374(v=vs.85)">CLUSPROP_DISK_SIGNATURE</a> 
          structure.



##### wType.CLUSPROP_TYPE_UNKNOWN (-1)

The type is unknown.



##### wType.CLUSPROP_TYPE_USER (32768 (0x8000))

Describes the beginning of the range for users to define their own types. Associate this type with 
          user-defined private properties.

## -remarks

To parse data that is returned from a 
     <a href="/previous-versions/windows/desktop/mscs/control-code-functions">control code function</a>, use the 
     <b>wFormat</b> member of this structure if the <b>wType</b> member 
     defines a type that the application cannot understand.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/creating-physical-disk-resources">Creating Physical Disk Resources</a> 
     and 
     <a href="/previous-versions/windows/desktop/mscs/building-with-clusprop-buffer-helper">Building with CLUSPROP_BUFFER_HELPER</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/ip-addresses-address">Address</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-class-info">CLUSCTL_RESOURCE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-class-info">CLUSCTL_RESOURCE_TYPE_GET_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-type-get-required-dependencies">CLUSCTL_RESOURCE_TYPE_GET_REQUIRED_DEPENDENCIES</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_dword">CLUSPROP_DISK_NUMBER</a>



<a href="/previous-versions/windows/desktop/legacy/aa368374(v=vs.85)">CLUSPROP_DISK_SIGNATURE</a>



<a href="/previous-versions/windows/desktop/legacy/aa368375(v=vs.85)">CLUSPROP_DWORD</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_filetime">CLUSPROP_FILETIME</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_long">CLUSPROP_LONG</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_sz">CLUSPROP_MULTI_SZ</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex">CLUSPROP_PARTITION_INFO_EX</a>



<a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class">CLUSPROP_RESOURCE_CLASS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a>



<b>CLUSPROP_ULARGE_INTEGER</b>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_format">CLUSTER_PROPERTY_FORMAT</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_syntax">CLUSTER_PROPERTY_SYNTAX</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_property_type">CLUSTER_PROPERTY_TYPE</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcetypecontrol">ClusterResourceTypeControl</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>



<a href="/previous-versions/windows/desktop/mscs/resources-name">Name (property for resources)</a>



<a href="/previous-versions/windows/desktop/mscs/nodes-nodename">NodeName</a>