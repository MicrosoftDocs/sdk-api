---
UID: NS:clusapi.CLUSPROP_BUFFER_HELPER
title: CLUSPROP_BUFFER_HELPER (clusapi.h)
description: Used to build or parse a property list or, a value list.
helpviewer_keywords: ["*PCLUSPROP_BUFFER_HELPER","CLUSPROP_BUFFER_HELPER","CLUSPROP_BUFFER_HELPER union [Failover Cluster]","PCLUSPROP_BUFFER_HELPER","PCLUSPROP_BUFFER_HELPER union pointer [Failover Cluster]","_wolf_clusprop_buffer_helper","clusapi/CLUSPROP_BUFFER_HELPER","clusapi/PCLUSPROP_BUFFER_HELPER","mscs.clusprop_buffer_helper"]
old-location: mscs\clusprop_buffer_helper.htm
tech.root: MsCS
ms.assetid: a2b706a0-76fe-4757-b76b-96cb6708bb61
ms.date: 12/05/2018
ms.keywords: '*PCLUSPROP_BUFFER_HELPER, CLUSPROP_BUFFER_HELPER, CLUSPROP_BUFFER_HELPER union [Failover Cluster], PCLUSPROP_BUFFER_HELPER, PCLUSPROP_BUFFER_HELPER union pointer [Failover Cluster], _wolf_clusprop_buffer_helper, clusapi/CLUSPROP_BUFFER_HELPER, clusapi/PCLUSPROP_BUFFER_HELPER, mscs.clusprop_buffer_helper'
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
req.typenames: CLUSPROP_BUFFER_HELPER, *PCLUSPROP_BUFFER_HELPER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSPROP_BUFFER_HELPER
 - clusapi/CLUSPROP_BUFFER_HELPER
 - PCLUSPROP_BUFFER_HELPER
 - clusapi/PCLUSPROP_BUFFER_HELPER
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
 - CLUSPROP_BUFFER_HELPER
---

# CLUSPROP_BUFFER_HELPER structure


## -description

Used to build or parse a <a href="/previous-versions/windows/desktop/mscs/property-lists">property list</a> or, a 
    <a href="/previous-versions/windows/desktop/mscs/value-lists">value list</a>.

## -struct-fields

### -field pb

Pointer to a buffer containing an array of bytes.

### -field pw

Pointer to a buffer containing an array of <b>WORD</b> values.

### -field pdw

Pointer to a buffer containing an array of <b>DWORD</b> values.

### -field pl

Pointer to a buffer containing an array of signed <b>long</b> values.

### -field psz

Pointer to a buffer containing a <b>NULL</b>-terminated Unicode string value.

### -field pList

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_list">CLUSPROP_LIST</a> structure describing the 
       beginning of a property list.

### -field pSyntax

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a> structure describing 
       the format and type of a value.

### -field pName

Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a> 
       structure containing a property name value.

### -field pValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure describing the 
       format, type, and length of a data value.

### -field pBinaryValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a> structure containing a 
       binary data value.

### -field pWordValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_word">CLUSPROP_WORD</a> structure containing a 
       numeric value.

### -field pDwordValue

Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa368375(v=vs.85)">CLUSPROP_DWORD</a> structure containing a 
       numeric value.

### -field pLongValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_long">CLUSPROP_LONG</a> structure containing a 
       signed long value.

### -field pULargeIntegerValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_ularge_integer">CLUSPROP_ULARGE_INTEGER</a> 
       structure containing an unsigned large integer value.

### -field pLargeIntegerValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_large_integer">CLUSPROP_LARGE_INTEGER</a> 
       structure containing a large integer value.

### -field pStringValue

Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a> structure containing a 
       <b>NULL</b>-terminated Unicode string value.

### -field pMultiSzValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_sz">CLUSPROP_MULTI_SZ</a> structure 
       containing multiple null-terminated Unicode string values.

### -field pSecurityDescriptor

Pointer to a 
       <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_security_descriptor">CLUSPROP_SECURITY_DESCRIPTOR</a> structure 
       containing a security descriptor.

### -field pResourceClassValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class">CLUSPROP_RESOURCE_CLASS</a> 
       structure containing a resource class value.

### -field pResourceClassInfoValue

Pointer to a 
       <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class_info">CLUSPROP_RESOURCE_CLASS_INFO</a> structure 
       containing a resource class information value.

### -field pDiskSignatureValue

Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa368374(v=vs.85)">CLUSPROP_DISK_SIGNATURE</a> 
       structure containing a disk signature value.

### -field pScsiAddressValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a> 
       structure containing an <a href="/previous-versions/windows/desktop/mscs/s-gly">SCSI</a> 
       address value.

### -field pDiskNumberValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_dword">CLUSPROP_DISK_NUMBER</a> structure 
       containing a disk number value.

### -field pPartitionInfoValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a> 
       structure containing a partition information value.

### -field pRequiredDependencyValue

Pointer to a 
       <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_required_dependency">CLUSPROP_REQUIRED_DEPENDENCY</a> structure 
       containing a resource dependency value.

### -field pPartitionInfoValueEx

Pointer to a 
       <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex">CLUSPROP_PARTITION_INFO_EX</a> structure 
       containing a partition information value.

### -field pPartitionInfoValueEx2

A pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info_ex2">CLUSPROP_PARTITION_INFO_EX2</a> structure 
       that contains a partition information value.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This member is not available before Windows Server 2016.

### -field pFileTimeValue

Pointer to a <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_filetime">CLUSPROP_FILETIME</a> structure 
       containing a date/time value.

## -remarks

The <b>CLUSPROP_BUFFER_HELPER</b> structure is useful 
     in working with property and value lists. Applications can use a generic 
     <b>CLUSPROP_BUFFER_HELPER</b> pointer to advance by 
     offsets through the entries of a property list or value list, retrieving or setting values without having to cast 
     to the appropriate data type.

An alternate structure, <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_property_item">RESUTIL_PROPERTY_ITEM</a>, 
     can also be used to work with multiple properties.

Use caution when referencing large integer values in <b>DWORD</b>-aligned structures 
     such as value lists, property lists, and 
     <a href="/previous-versions/windows/desktop/mscs/parameter-blocks">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0 or 8h. 
     <b>DWORD</b> alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or C), which will cause an alignment fault when the data is read or written. You can avoid alignment 
     faults by handling the high and low parts of large values separately, or by using local variables, which are 
     guaranteed to be naturally aligned.


#### Examples

In addition to the following example, see 
      <a href="/previous-versions/windows/desktop/mscs/creating-property-lists">Creating Property Lists</a>, 
      <a href="/previous-versions/windows/desktop/mscs/parsing-property-lists">Parsing Property Lists</a>, 
      <a href="/previous-versions/windows/desktop/mscs/creating-value-lists">Creating Value Lists</a>, and 
      <a href="/previous-versions/windows/desktop/mscs/parsing-a-value-list">Parsing a Value List</a>.


```cpp
//////////////////////////////////////////////////////////////////////
//  
//    HOW TO USE CLUSPROP_BUFFER HELPER
//  
//    (1) Position cbh to the next read or write location.
//    (2) Read or write data using an appropriate pointer.
//    (3) Check position within buffer.
//  
//    Repeat (1)(2)(3)
//    
//////////////////////////////////////////////////////////////////////
void ClusDocEx_UsingCBH()
{
    LPVOID lp = LocalAlloc( LPTR, 100 ); // It is important for cbh
                                         // to know the allocated
                                         // size.
    CLUSPROP_BUFFER_HELPER cbh;

   
// ( 1 )
//
//    Position cbh.  The pb member is convenient for
//    targeting single bytes.
//

      cbh.pb = (LPBYTE) lp;     


//
//    The pb member points to the first byte of lp.
//
//    lp -----> 0 0 0 0 0 0 0 0 0 0 0 ... 0 
//
//    cbh.pb-->|-|
//
//
//    Note what happens when different cbh pointer types are used:
//
//                   lp -----> 0 0 0 0 0 0 0 0 0 0 0 0 ... 0 
//
//    cbh.pdw              -->|-------|
//    cbh.psz              -->|-|
//    cbh.pValue           -->|---------------|
//    cbh.pValue->Syntax.dw-->|-------|
//    cbh.pValue->cbLength         -->|-------|
//
//
//    The configuration of bytes that will be affected by a read
//    or write operation depends on the type of pointer used.
//


// ( 2 )
//
//    Read or write data to the present location.  Note how the
//    structure pointers let you "reach over" intervening members.
//

      cbh.pValue->Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_DWORD; 
    
      cbh.pValue->cbLength = sizeof( DWORD );

      cbh.pDwordValue->dw  = 0x0000EEEEL;

//
//    Result:   lp ----->| syntax | length |  value  | 0 0 0 0 ... 0 
//


// ( 3 )
//
//    Check your remaining space.  Be sure you have room to advance
//    cbh past the current data and perform a read operation on the
//    next value.
//
      
      DWORD cbPosition = cbh.pb - (LPBYTE) lp;

      DWORD cbAdvance = ClusDocEx_ListEntrySize( sizeof( DWORD ) );  // See "ClusDocEx.h"

      if( ( cbPosition + cbAdvance + sizeof( DWORD ) ) > 100 )
      {
          // handle the fact that there's more data than the reported size of the buffer
      }

//
//    Repeat ( 1 ), ( 2 ), and ( 3 ) for the next value:
// 

      // Position cbh

      cbh.pb += cbAdvance;


      // Write next entry

      cbh.pStringValue->Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;

      cbh.pStringValue->cbLength = ( lstrlenW( L"String Value" ) + 1 ) * sizeof( WCHAR );
      
      StringCchCopyW( cbh.pStringValue->sz, cbh.pStringValue->cbLength, L"String Value" );


      // Check space
      
      cbPosition = cbh.pb - (LPBYTE) lp;

      cbAdvance = ClusDocEx_ListEntrySize( cbh.pStringValue->cbLength ); 

      if( ( cbPosition + cbAdvance + sizeof( DWORD ) ) > 100 )
      {
          // 
      }

//
//    Repeat ( 1 ), ( 2 ), and ( 3 )  until all values have been written or read.
//


      cbh.pb = NULL;

      LocalFree( lp );
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_binary">CLUSPROP_BINARY</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_dword">CLUSPROP_DISK_NUMBER</a>



<a href="/previous-versions/windows/desktop/legacy/aa368374(v=vs.85)">CLUSPROP_DISK_SIGNATURE</a>



<a href="/previous-versions/windows/desktop/legacy/aa368375(v=vs.85)">CLUSPROP_DWORD</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_list">CLUSPROP_LIST</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_sz">CLUSPROP_MULTI_SZ</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_partition_info">CLUSPROP_PARTITION_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa368382(v=vs.85)">CLUSPROP_PROPERTY_NAME</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_required_dependency">CLUSPROP_REQUIRED_DEPENDENCY</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class">CLUSPROP_RESOURCE_CLASS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_resource_class_info">CLUSPROP_RESOURCE_CLASS_INFO</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_scsi_address">CLUSPROP_SCSI_ADDRESS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>



<a href="/previous-versions/windows/desktop/legacy/aa368390(v=vs.85)">CLUSPROP_SZ</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_ularge_integer">CLUSPROP_ULARGE_INTEGER</a>



<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a>