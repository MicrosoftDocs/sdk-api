---
UID: NF:winddi.EngQuerySystemAttribute
title: EngQuerySystemAttribute function (winddi.h)
description: The EngQuerySystemAttribute function queries processor-specific or system-specific capabilities.
helpviewer_keywords: ["EngQuerySystemAttribute","EngQuerySystemAttribute function [Display Devices]","display.engquerysystemattribute","gdifncs_8d196296-10a2-4118-9318-fe0267df4e60.xml","winddi/EngQuerySystemAttribute"]
old-location: display\engquerysystemattribute.htm
tech.root: display
ms.assetid: 7559075d-f2df-4c71-9523-22417d5cfd5a
ms.date: 12/05/2018
ms.keywords: EngQuerySystemAttribute, EngQuerySystemAttribute function [Display Devices], display.engquerysystemattribute, gdifncs_8d196296-10a2-4118-9318-fe0267df4e60.xml, winddi/EngQuerySystemAttribute
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngQuerySystemAttribute
 - winddi/EngQuerySystemAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngQuerySystemAttribute
---

# EngQuerySystemAttribute function


## -description

The <b>EngQuerySystemAttribute</b> function queries processor-specific or system-specific capabilities.

## -parameters

### -param CapNum [in]

Specifies the capability being queried. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>EngNumberOfProcessors</b>

</td>
<td>
GDI returns the number of active processors in the system.

</td>
</tr>
<tr>
<td>
<b>EngOptimumAvailableSystemMemory</b>

</td>
<td>
Not available for use.

</td>
</tr>
<tr>
<td>
<b>EngOptimumAvailableUserMemory</b>

</td>
<td>
Not available for use.

</td>
</tr>
<tr>
<td>
<b>EngProcessorFeature</b>

</td>
<td>
GDI returns a bitmask of flags that describe the features of the processor. Currently, GDI sets the QSA_MMX flag when an <i>x86</i> processor has MMX support. QSA_MMX is relevant only on the <i>x86</i> platform.

</td>
</tr>
</table>

### -param pCapability [out]

Pointer to the location that receives the result of the query. The value that GDI places in this parameter depends on the enumerated value specified by <i>CapNum</i>.

## -returns

<b>EngQuerySystemAttribute</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.

