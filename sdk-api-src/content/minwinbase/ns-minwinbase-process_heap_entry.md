---
UID: NS:minwinbase._PROCESS_HEAP_ENTRY
title: PROCESS_HEAP_ENTRY (minwinbase.h)
description: Contains information about a heap element.
helpviewer_keywords: ["*LPPROCESS_HEAP_ENTRY","*PPROCESS_HEAP_ENTRY","LPPROCESS_HEAP_ENTRY","LPPROCESS_HEAP_ENTRY structure pointer","PROCESS_HEAP_ENTRY","PROCESS_HEAP_ENTRY structure","PROCESS_HEAP_ENTRY_BUSY","PROCESS_HEAP_ENTRY_DDESHARE","PROCESS_HEAP_ENTRY_MOVEABLE","PROCESS_HEAP_REGION","PROCESS_HEAP_UNCOMMITTED_RANGE","_PROCESS_HEAP_ENTRY","_win32_process_heap_entry_str","base.process_heap_entry_str","minwinbase/LPPROCESS_HEAP_ENTRY","minwinbase/PROCESS_HEAP_ENTRY"]
old-location: base\process_heap_entry_str.htm
tech.root: base
ms.assetid: e61b209a-9cc1-4171-9638-5456b0fcf775
ms.date: 12/05/2018
ms.keywords: '*LPPROCESS_HEAP_ENTRY, *PPROCESS_HEAP_ENTRY, LPPROCESS_HEAP_ENTRY, LPPROCESS_HEAP_ENTRY structure pointer, PROCESS_HEAP_ENTRY, PROCESS_HEAP_ENTRY structure, PROCESS_HEAP_ENTRY_BUSY, PROCESS_HEAP_ENTRY_DDESHARE, PROCESS_HEAP_ENTRY_MOVEABLE, PROCESS_HEAP_REGION, PROCESS_HEAP_UNCOMMITTED_RANGE, _PROCESS_HEAP_ENTRY, _win32_process_heap_entry_str, base.process_heap_entry_str, minwinbase/LPPROCESS_HEAP_ENTRY, minwinbase/PROCESS_HEAP_ENTRY'
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PROCESS_HEAP_ENTRY, *LPPROCESS_HEAP_ENTRY, *PPROCESS_HEAP_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROCESS_HEAP_ENTRY
 - minwinbase/_PROCESS_HEAP_ENTRY
 - LPPROCESS_HEAP_ENTRY
 - minwinbase/LPPROCESS_HEAP_ENTRY
 - PROCESS_HEAP_ENTRY
 - minwinbase/PROCESS_HEAP_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - PROCESS_HEAP_ENTRY
---

# PROCESS_HEAP_ENTRY structure


## -description

Contains information about a heap element. The 
    <a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> function uses a 
    <b>PROCESS_HEAP_ENTRY</b> structure to enumerate the 
    elements of a heap.

## -struct-fields

### -field lpData

A pointer to the data portion of the heap element.

To initiate a <a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> heap enumeration, set 
       <b>lpData</b> to <b>NULL</b>.

If <b>PROCESS_HEAP_REGION</b> is used in the <b>wFlags</b> member, 
       <b>lpData</b> points to the first virtual address used by the region.

If <b>PROCESS_HEAP_UNCOMMITTED_RANGE</b> is used in <b>wFlags</b>, 
       <b>lpData</b> points to the beginning of the range of uncommitted memory.

### -field cbData

The size of the data portion of the heap element, in bytes.

If <b>PROCESS_HEAP_REGION</b> is used in <b>wFlags</b>, 
       <b>cbData</b> specifies the total size, in bytes, of the address space that is reserved for 
       this region.

If <b>PROCESS_HEAP_UNCOMMITTED_RANGE</b> is used in <b>wFlags</b>, 
       <b>cbData</b> specifies the size, in bytes, of the range of uncommitted memory.

### -field cbOverhead

The size of the data used by the system to maintain information about the heap element, in bytes. These 
       overhead bytes are in addition to the <b>cbData</b> bytes of the data portion of the heap 
       element.

If <b>PROCESS_HEAP_REGION</b> is used in <b>wFlags</b>, 
       <b>cbOverhead</b> specifies the size, in bytes, of the heap control structures that 
       describe the region.

If <b>PROCESS_HEAP_UNCOMMITTED_RANGE</b> is used in <b>wFlags</b>, 
       <b>cbOverhead</b> specifies the size, in bytes, of the control structures that describe 
       this uncommitted range.

### -field iRegionIndex

A handle to the heap region that contains the heap element. A heap consists of one or more regions of virtual 
       memory, each with a unique region index.

In the first heap entry returned for most heap regions, 
       <a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> uses the 
       <b>PROCESS_HEAP_REGION</b> in the <b>wFlags</b> member. When this value 
       is used, the members of the <b>Region</b> structure contain additional information 
       about the region.

The <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function sometimes uses the 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a> function to allocate large blocks from a 
       growable heap. The heap manager treats such a large block allocation as a separate region with a unique region 
       index. <a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a> does not use 
       <b>PROCESS_HEAP_REGION</b> in the heap entry returned for a large block region, so the 
       members of the <b>Region</b> structure are not valid. You can use the 
       <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a> function to get additional information 
       about a large block region.

### -field wFlags

The properties of the heap element. Some values affect the meaning of other members of this 
       <b>PROCESS_HEAP_ENTRY</b> data structure. The 
       following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESS_HEAP_ENTRY_BUSY"></a><a id="process_heap_entry_busy"></a><dl>
<dt><b>PROCESS_HEAP_ENTRY_BUSY</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The heap element is an allocated block.

If <b>PROCESS_HEAP_ENTRY_MOVEABLE</b> is also specified, the 
         <b>Block</b> structure becomes valid. The <b>hMem</b> member of 
         the <b>Block</b> structure contains a handle to the allocated, moveable memory 
         block.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_HEAP_ENTRY_DDESHARE"></a><a id="process_heap_entry_ddeshare"></a><dl>
<dt><b>PROCESS_HEAP_ENTRY_DDESHARE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
This value must be used with <b>PROCESS_HEAP_ENTRY_BUSY</b>, indicating that the heap 
        element is an allocated block.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_HEAP_ENTRY_MOVEABLE"></a><a id="process_heap_entry_moveable"></a><dl>
<dt><b>PROCESS_HEAP_ENTRY_MOVEABLE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
This value must be used with <b>PROCESS_HEAP_ENTRY_BUSY</b>, indicating that the heap 
         element is an allocated block.

The block was allocated with <b>LMEM_MOVEABLE</b> or 
         <b>GMEM_MOVEABLE</b>, and the <b>Block</b> structure becomes 
         valid. The <b>hMem</b> member of the <b>Block</b> structure 
         contains a handle to the allocated, moveable memory block.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_HEAP_REGION"></a><a id="process_heap_region"></a><dl>
<dt><b>PROCESS_HEAP_REGION</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The heap element is located at the beginning of a region of contiguous virtual memory in use by the heap.

The <b>lpData</b> member of the structure points to the first virtual address used by 
         the region; the <b>cbData</b> member specifies the total size, in bytes, of the address 
         space that is reserved for this region; and the <b>cbOverhead</b> member specifies the 
         size, in bytes, of the heap control structures that describe the region.

The <b>Region</b> structure becomes valid. The 
         <b>dwCommittedSize</b>, <b>dwUnCommittedSize</b>, 
         <b>lpFirstBlock</b>, and <b>lpLastBlock</b> members of the structure 
         contain additional information about the region.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_HEAP_UNCOMMITTED_RANGE"></a><a id="process_heap_uncommitted_range"></a><dl>
<dt><b>PROCESS_HEAP_UNCOMMITTED_RANGE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The heap element is located in a range of uncommitted memory within the heap region.

The <b>lpData</b> member points to the beginning of the range of uncommitted memory; 
         the <b>cbData</b> member specifies the size, in bytes, of the range of uncommitted 
         memory; and the <b>cbOverhead</b> member specifies the size, in bytes, of the control 
         structures that describe this uncommitted range.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Block

This structure is valid only if both the <b>PROCESS_HEAP_ENTRY_BUSY</b> and 
        <b>PROCESS_HEAP_ENTRY_MOVEABLE</b> are specified in <b>wFlags</b>.

### -field DUMMYUNIONNAME.Block.hMem

Handle to the allocated, moveable memory block.

### -field DUMMYUNIONNAME.Block.dwReserved

Reserved; not used.

### -field DUMMYUNIONNAME.Region

This structure is valid only if the <b>wFlags</b> member specifies 
        <b>PROCESS_HEAP_REGION</b>.

### -field DUMMYUNIONNAME.Region.dwCommittedSize

Number of bytes in the heap region that are currently committed as free memory blocks, busy memory blocks, 
         or heap control structures.

This is an optional field that is set to zero if the number of committed bytes is not available.

### -field DUMMYUNIONNAME.Region.dwUnCommittedSize

Number of bytes in the heap region that are currently uncommitted.

This is an optional field that is set to zero if the number of uncommitted bytes is not available.

### -field DUMMYUNIONNAME.Region.lpFirstBlock

Pointer to the first valid memory block in this heap region.

### -field DUMMYUNIONNAME.Region.lpLastBlock

Pointer to the first invalid memory block in this heap region.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapwalk">HeapWalk</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc">VirtualAlloc</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualquery">VirtualQuery</a>