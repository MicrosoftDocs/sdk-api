---
UID: NF:oleauto.SafeArrayAllocDescriptorEx
title: SafeArrayAllocDescriptorEx function
author: windows-driver-content
description: Creates a safe array descriptor for an array of any valid variant type, including VT_RECORD, without allocating the array data.
old-location: automat\safearrayallocdescriptorex.htm
old-project: automat
ms.assetid: c368d278-ef62-4cf3-a7f8-c48549207c09
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: SafeArrayAllocDescriptorEx, SafeArrayAllocDescriptorEx function [Automation], _oa96_SafeArrayAllocDescriptorEx, automat.safearrayallocdescriptorex, oleauto/SafeArrayAllocDescriptorEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	SafeArrayAllocDescriptorEx
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SafeArrayAllocDescriptorEx function


## -description


Creates a safe array descriptor for an array of any valid variant type, including VT_RECORD, without allocating the array data.


## -parameters




### -param vt [in]

The variant type.


### -param cDims [in]

The number of dimensions in the array.


### -param ppsaOut [out]

The safe array descriptor.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> was not valid.

</td>
</tr>
</table>
 




## -remarks



Because <a href="https://msdn.microsoft.com/8fe5c802-cdc0-4e7a-9410-ba65f9a5140e">SafeArrayAllocDescriptor</a> does not take a VARTYPE, it is not possible to use it to create the safe array descriptor for an array of records. The <b>SafeArrayAllocDescriptorEx</b> is used to allocate a safe array descriptor for an array of records of the given dimensions.



