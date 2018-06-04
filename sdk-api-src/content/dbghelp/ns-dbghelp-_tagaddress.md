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

# _tagADDRESS structure


## -description


Represents an address. It is used in the 
<a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a> structure.


## -struct-fields




### -field Offset

The offset into the segment, or a 32-bit virtual address. The interpretation of this value depends on the value contained in the <b>Mode</b> member.


### -field Segment

The segment number. This value is used only for 16-bit addressing.


### -field Mode

The addressing mode. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AddrMode1616"></a><a id="addrmode1616"></a><a id="ADDRMODE1616"></a><dl>
<dt><b>AddrMode1616</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
16:16 addressing. To support this addressing mode, you must supply a 
<a href="https://msdn.microsoft.com/56c374df-6b48-4649-a914-5cb2f9575bf3">TranslateAddressProc64</a> callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="AddrMode1632"></a><a id="addrmode1632"></a><a id="ADDRMODE1632"></a><dl>
<dt><b>AddrMode1632</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
16:32 addressing. To support this addressing mode, you must supply a 
<a href="https://msdn.microsoft.com/56c374df-6b48-4649-a914-5cb2f9575bf3">TranslateAddressProc64</a> callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="AddrModeReal"></a><a id="addrmodereal"></a><a id="ADDRMODEREAL"></a><dl>
<dt><b>AddrModeReal</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Real-mode addressing. To support this addressing mode, you must supply a 
<a href="https://msdn.microsoft.com/56c374df-6b48-4649-a914-5cb2f9575bf3">TranslateAddressProc64</a> callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="AddrModeFlat"></a><a id="addrmodeflat"></a><a id="ADDRMODEFLAT"></a><dl>
<dt><b>AddrModeFlat</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Flat addressing. This is the only addressing mode supported by the library.

</td>
</tr>
</table>
 


## -remarks



This structure supersedes the <b>ADDRESS</b> structure. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>ADDRESS</b> is defined as follows in DbgHelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
#define ADDRESS ADDRESS64
#define LPADDRESS LPADDRESS64
#else
typedef struct _tagADDRESS {
    DWORD         Offset;
    WORD          Segment;
    ADDRESS_MODE  Mode;
} ADDRESS, *LPADDRESS;
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a>
 

 

