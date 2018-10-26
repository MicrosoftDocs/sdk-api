---
UID: NS:clusapi.CLUSPROP_BUFFER_HELPER
title: CLUSPROP_BUFFER_HELPER
author: windows-sdk-content
description: Used to build or parse a property list or, a value list.
old-location: mscs\clusprop_buffer_helper.htm
tech.root: mscs
ms.assetid: a2b706a0-76fe-4757-b76b-96cb6708bb61
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PCLUSPROP_BUFFER_HELPER, CLUSPROP_BUFFER_HELPER, CLUSPROP_BUFFER_HELPER union [Failover Cluster], PCLUSPROP_BUFFER_HELPER, PCLUSPROP_BUFFER_HELPER union pointer [Failover Cluster], _wolf_clusprop_buffer_helper, clusapi/CLUSPROP_BUFFER_HELPER, clusapi/PCLUSPROP_BUFFER_HELPER, mscs.clusprop_buffer_helper"
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
 - CLUSPROP_BUFFER_HELPER
product: Windows
targetos: Windows
req.typenames: CLUSPROP_BUFFER_HELPER, *PCLUSPROP_BUFFER_HELPER
req.redist: 
---

# CLUSPROP_BUFFER_HELPER structure


## -description


Used to build or parse a <a href="https://msdn.microsoft.com/57312b32-01cf-48e8-b61f-6095e23bb580">property list</a> or, a 
    <a href="https://msdn.microsoft.com/f2b20fe5-0d7e-4ccd-b288-aa8104a24fef">value list</a>.


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

Pointer to a <a href="https://msdn.microsoft.com/1f76104f-99eb-4376-8d92-e04b7f00c46d">CLUSPROP_LIST</a> structure describing the 
       beginning of a property list.


### -field pSyntax

Pointer to a <a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a> structure describing 
       the format and type of a value.


### -field pName

Pointer to a <a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a> 
       structure containing a property name value.


### -field pValue

Pointer to a <a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a> structure describing the 
       format, type, and length of a data value.


### -field pBinaryValue

Pointer to a <a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a> structure containing a 
       binary data value.


### -field pWordValue

Pointer to a <a href="https://msdn.microsoft.com/ba09290b-171b-45cf-a367-485f7322ebef">CLUSPROP_WORD</a> structure containing a 
       numeric value.


### -field pDwordValue

Pointer to a <a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a> structure containing a 
       numeric value.


### -field pLongValue

Pointer to a <a href="https://msdn.microsoft.com/aa214e43-cadc-4f06-8c98-e6a5b13258b8">CLUSPROP_LONG</a> structure containing a 
       signed long value.


### -field pULargeIntegerValue

Pointer to a <a href="https://msdn.microsoft.com/1db28e46-e5e0-4d99-b9a8-80c3f1534ca6">CLUSPROP_ULARGE_INTEGER</a> 
       structure containing an unsigned large integer value.


### -field pLargeIntegerValue

Pointer to a <a href="https://msdn.microsoft.com/3e0849e6-3d93-47cb-858d-9891451b8dfd">CLUSPROP_LARGE_INTEGER</a> 
       structure containing a large integer value.


### -field pStringValue

Pointer to a <a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a> structure containing a 
       <b>NULL</b>-terminated Unicode string value.


### -field pMultiSzValue

Pointer to a <a href="https://msdn.microsoft.com/3c508ed6-eec8-4fa9-9ae7-9c8d7f4c8b98">CLUSPROP_MULTI_SZ</a> structure 
       containing multiple null-terminated Unicode string values.


### -field pSecurityDescriptor

Pointer to a 
       <a href="https://msdn.microsoft.com/b19358cf-1cf9-4d91-85df-ed7fa804a7f2">CLUSPROP_SECURITY_DESCRIPTOR</a> structure 
       containing a security descriptor.


### -field pResourceClassValue

Pointer to a <a href="https://msdn.microsoft.com/9ec01908-3765-4e95-a9d3-fdf6daa5f64d">CLUSPROP_RESOURCE_CLASS</a> 
       structure containing a resource class value.


### -field pResourceClassInfoValue

Pointer to a 
       <a href="https://msdn.microsoft.com/449f297e-6207-446e-ac80-03145c44d671">CLUSPROP_RESOURCE_CLASS_INFO</a> structure 
       containing a resource class information value.


### -field pDiskSignatureValue

Pointer to a <a href="https://msdn.microsoft.com/38400cce-d84a-4439-9dab-20102c1580ff">CLUSPROP_DISK_SIGNATURE</a> 
       structure containing a disk signature value.


### -field pScsiAddressValue

Pointer to a <a href="https://msdn.microsoft.com/30907886-0c86-4e8a-9a95-5b62f6ffff76">CLUSPROP_SCSI_ADDRESS</a> 
       structure containing an <a href="s_gly.htm">SCSI</a> 
       address value.


### -field pDiskNumberValue

Pointer to a <a href="https://msdn.microsoft.com/8230d356-0d5a-4859-ae03-c25d078684b3">CLUSPROP_DISK_NUMBER</a> structure 
       containing a disk number value.


### -field pPartitionInfoValue

Pointer to a <a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a> 
       structure containing a partition information value.


### -field pRequiredDependencyValue

Pointer to a 
       <a href="https://msdn.microsoft.com/dae7544d-31c0-4a4b-8acb-d652bae817dd">CLUSPROP_REQUIRED_DEPENDENCY</a> structure 
       containing a resource dependency value.


### -field pPartitionInfoValueEx

Pointer to a 
       <a href="https://msdn.microsoft.com/b1343a04-b8bd-469a-a620-985eeb89401c">CLUSPROP_PARTITION_INFO_EX</a> structure 
       containing a partition information value.


### -field pPartitionInfoValueEx2

A pointer to a <a href="https://msdn.microsoft.com/D6D26335-80D0-4949-99B4-FE18DD2FFF3C">CLUSPROP_PARTITION_INFO_EX2</a> structure 
       that contains a partition information value.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This member is not available before Windows Server 2016.




### -field pFileTimeValue

Pointer to a <a href="https://msdn.microsoft.com/2c88e9db-f218-4b88-9bb0-607fd09e8d0b">CLUSPROP_FILETIME</a> structure 
       containing a date/time value.


## -remarks



The <b>CLUSPROP_BUFFER_HELPER</b> structure is useful 
     in working with property and value lists. Applications can use a generic 
     <b>CLUSPROP_BUFFER_HELPER</b> pointer to advance by 
     offsets through the entries of a property list or value list, retrieving or setting values without having to cast 
     to the appropriate data type.

An alternate structure, <a href="https://msdn.microsoft.com/f65ee50f-59f7-44db-ad69-b29b3e693c7e">RESUTIL_PROPERTY_ITEM</a>, 
     can also be used to work with multiple properties.

Use caution when referencing large integer values in <b>DWORD</b>-aligned structures 
     such as value lists, property lists, and 
     <a href="https://msdn.microsoft.com/fd77397b-36dd-4a20-b3f4-7dbbee1fd787">parameter blocks</a>. For Windows Server for Itanium-based 
     systems, a naturally-aligned large integer value always begins on an address ending in 0 or 8h. 
     <b>DWORD</b> alignment can cause large values to begin on unaligned boundaries (addresses 
     ending in 4h or C), which will cause an alignment fault when the data is read or written. You can avoid alignment 
     faults by handling the high and low parts of large values separately, or by using local variables, which are 
     guaranteed to be naturally aligned.


#### Examples

In addition to the following example, see 
      <a href="https://msdn.microsoft.com/15d08ce0-070a-47cd-bf0c-71fdc98d6d7f">Creating Property Lists</a>, 
      <a href="https://msdn.microsoft.com/fde017dc-fcc8-4b34-a56a-85f052306569">Parsing Property Lists</a>, 
      <a href="https://msdn.microsoft.com/7af7f5a8-fe1f-4b2a-9332-fd2cefc18cc2">Creating Value Lists</a>, and 
      <a href="https://msdn.microsoft.com/3504b04d-9b96-4b44-a8ae-f5e5eb8231d8">Parsing a Value List</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//////////////////////////////////////////////////////////////////////
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
//    lp -----&gt; 0 0 0 0 0 0 0 0 0 0 0 ... 0 
//
//    cbh.pb--&gt;|-|
//
//
//    Note what happens when different cbh pointer types are used:
//
//                   lp -----&gt; 0 0 0 0 0 0 0 0 0 0 0 0 ... 0 
//
//    cbh.pdw              --&gt;|-------|
//    cbh.psz              --&gt;|-|
//    cbh.pValue           --&gt;|---------------|
//    cbh.pValue-&gt;Syntax.dw--&gt;|-------|
//    cbh.pValue-&gt;cbLength         --&gt;|-------|
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

      cbh.pValue-&gt;Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_DWORD; 
    
      cbh.pValue-&gt;cbLength = sizeof( DWORD );

      cbh.pDwordValue-&gt;dw  = 0x0000EEEEL;

//
//    Result:   lp -----&gt;| syntax | length |  value  | 0 0 0 0 ... 0 
//


// ( 3 )
//
//    Check your remaining space.  Be sure you have room to advance
//    cbh past the current data and perform a read operation on the
//    next value.
//
      
      DWORD cbPosition = cbh.pb - (LPBYTE) lp;

      DWORD cbAdvance = ClusDocEx_ListEntrySize( sizeof( DWORD ) );  // See "ClusDocEx.h"

      if( ( cbPosition + cbAdvance + sizeof( DWORD ) ) &gt; 100 )
      {
          // handle the fact that there's more data than the reported size of the buffer
      }

//
//    Repeat ( 1 ), ( 2 ), and ( 3 ) for the next value:
// 

      // Position cbh

      cbh.pb += cbAdvance;


      // Write next entry

      cbh.pStringValue-&gt;Syntax.dw = CLUSPROP_SYNTAX_LIST_VALUE_SZ;

      cbh.pStringValue-&gt;cbLength = ( lstrlenW( L"String Value" ) + 1 ) * sizeof( WCHAR );
      
      StringCchCopyW( cbh.pStringValue-&gt;sz, cbh.pStringValue-&gt;cbLength, L"String Value" );


      // Check space
      
      cbPosition = cbh.pb - (LPBYTE) lp;

      cbAdvance = ClusDocEx_ListEntrySize( cbh.pStringValue-&gt;cbLength ); 

      if( ( cbPosition + cbAdvance + sizeof( DWORD ) ) &gt; 100 )
      {
          // 
      }

//
//    Repeat ( 1 ), ( 2 ), and ( 3 )  until all values have been written or read.
//


      cbh.pb = NULL;

      LocalFree( lp );
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/61169871-4998-4e9f-97dc-77344bbfa962">CLUSPROP_BINARY</a>



<a href="https://msdn.microsoft.com/8230d356-0d5a-4859-ae03-c25d078684b3">CLUSPROP_DISK_NUMBER</a>



<a href="https://msdn.microsoft.com/38400cce-d84a-4439-9dab-20102c1580ff">CLUSPROP_DISK_SIGNATURE</a>



<a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a>



<a href="https://msdn.microsoft.com/1f76104f-99eb-4376-8d92-e04b7f00c46d">CLUSPROP_LIST</a>



<a href="https://msdn.microsoft.com/3c508ed6-eec8-4fa9-9ae7-9c8d7f4c8b98">CLUSPROP_MULTI_SZ</a>



<a href="https://msdn.microsoft.com/cda1e334-dba8-4fe9-b035-4e475245869c">CLUSPROP_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/bb2e904c-2782-45f6-b95d-b1b107fa0060">CLUSPROP_PROPERTY_NAME</a>



<a href="https://msdn.microsoft.com/dae7544d-31c0-4a4b-8acb-d652bae817dd">CLUSPROP_REQUIRED_DEPENDENCY</a>



<a href="https://msdn.microsoft.com/9ec01908-3765-4e95-a9d3-fdf6daa5f64d">CLUSPROP_RESOURCE_CLASS</a>



<a href="https://msdn.microsoft.com/449f297e-6207-446e-ac80-03145c44d671">CLUSPROP_RESOURCE_CLASS_INFO</a>



<a href="https://msdn.microsoft.com/30907886-0c86-4e8a-9a95-5b62f6ffff76">CLUSPROP_SCSI_ADDRESS</a>



<a href="https://msdn.microsoft.com/23353e11-63bb-4d3b-90fb-e2a5544e0d09">CLUSPROP_SYNTAX</a>



<a href="https://msdn.microsoft.com/f991ac6f-5272-44ee-a035-c9501bf7d866">CLUSPROP_SZ</a>



<a href="https://msdn.microsoft.com/1db28e46-e5e0-4d99-b9a8-80c3f1534ca6">CLUSPROP_ULARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/a77a51aa-2d2a-4b21-9f87-87dcf95fa0cd">CLUSPROP_VALUE</a>
 

 

