---
UID: NS:psapi._PSAPI_WORKING_SET_BLOCK
title: PSAPI_WORKING_SET_BLOCK (psapi.h)
description: Contains working set information for a page.
helpviewer_keywords: ["*PPSAPI_WORKING_SET_BLOCK","PPSAPI_WORKING_SET_BLOCK","PPSAPI_WORKING_SET_BLOCK union pointer [PSAPI]","PSAPI_WORKING_SET_BLOCK","PSAPI_WORKING_SET_BLOCK union [PSAPI]","base.psapi_working_set_block","psapi.psapi_working_set_block","psapi/PPSAPI_WORKING_SET_BLOCK","psapi/PSAPI_WORKING_SET_BLOCK"]
old-location: psapi\psapi_working_set_block.htm
tech.root: psapi
ms.assetid: feb64235-1003-4595-a6a9-aca1f94f94b8
ms.date: 12/05/2018
ms.keywords: '*PPSAPI_WORKING_SET_BLOCK, PPSAPI_WORKING_SET_BLOCK, PPSAPI_WORKING_SET_BLOCK union pointer [PSAPI], PSAPI_WORKING_SET_BLOCK, PSAPI_WORKING_SET_BLOCK union [PSAPI], base.psapi_working_set_block, psapi.psapi_working_set_block, psapi/PPSAPI_WORKING_SET_BLOCK, psapi/PSAPI_WORKING_SET_BLOCK'
req.header: psapi.h
req.include-header: 
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
req.typenames: PSAPI_WORKING_SET_BLOCK, *PPSAPI_WORKING_SET_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSAPI_WORKING_SET_BLOCK
 - psapi/_PSAPI_WORKING_SET_BLOCK
 - PPSAPI_WORKING_SET_BLOCK
 - psapi/PPSAPI_WORKING_SET_BLOCK
 - PSAPI_WORKING_SET_BLOCK
 - psapi/PSAPI_WORKING_SET_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - PSAPI_WORKING_SET_BLOCK
---

# PSAPI_WORKING_SET_BLOCK structure


## -description

Contains working set information for a page.

## -struct-fields

### -field Flags

The working set information. See the description of the structure  members for information about the layout of this variable.

### -field Protection

The protection attributes of the page. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The page is not accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Executable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Executable and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Executable and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Executable and copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The page is not accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Non-cacheable and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Non-cacheable and executable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, executable, and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Non-cacheable and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>13</dt>
</dl>
</td>
<td width="60%">
Non-cacheable and copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>14</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, executable, and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>15</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, executable, and copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The page is not accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>17</dt>
</dl>
</td>
<td width="60%">
Guard page and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>18</dt>
</dl>
</td>
<td width="60%">
Guard page and executable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>19</dt>
</dl>
</td>
<td width="60%">
Guard page, executable, and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>20</dt>
</dl>
</td>
<td width="60%">
Guard page and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>21</dt>
</dl>
</td>
<td width="60%">
Guard page and copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>22</dt>
</dl>
</td>
<td width="60%">
Guard page, executable, and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>23</dt>
</dl>
</td>
<td width="60%">
Guard page, executable, and copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>24</dt>
</dl>
</td>
<td width="60%">
The page is not accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>25</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>26</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, and executable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>27</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, executable, and read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>28</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>29</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, and copy-on-write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>30</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, executable, and read/write.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>31</dt>
</dl>
</td>
<td width="60%">
Non-cacheable, guard page, executable, and copy-on-write.

</td>
</tr>
</table>

### -field ShareCount

The number of processes that share this page. The maximum value of this member is 7.

### -field Shared

If this bit is 1, the page is sharable; otherwise, the page is not sharable.

### -field Reserved

This member is reserved.

### -field VirtualPage

The address of the page in the virtual address space.

<b>64-bit Windows:  </b>This member is 52 bits in length.

## -see-also

<a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_information">PSAPI_WORKING_SET_INFORMATION</a>