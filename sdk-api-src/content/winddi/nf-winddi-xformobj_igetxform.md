---
UID: NF:winddi.XFORMOBJ_iGetXform
title: XFORMOBJ_iGetXform function
author: windows-sdk-content
description: The XFORMOBJ_iGetXform function downloads a transform to the driver.
old-location: display\xformobj_igetxform.htm
tech.root: display
ms.assetid: 0a78663c-15c9-4fed-b758-fea0f2571971
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: XFORMOBJ_iGetXform, XFORMOBJ_iGetXform function [Display Devices], display.xformobj_igetxform, gdifncs_b011606a-15e6-4f4f-a6ce-37ad087788c4.xml, winddi/XFORMOBJ_iGetXform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - XFORMOBJ_iGetXform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XFORMOBJ_iGetXform function


## -description


The <b>XFORMOBJ_iGetXform</b> function downloads a transform to the driver.


## -parameters




### -param pxo

Pointer to the <a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a> structure that defines the transform to be downloaded to the driver.


### -param pxform

Pointer to the buffer that is to receive the <a href="https://msdn.microsoft.com/5abfd19b-c946-45df-ae3b-b872ef706dd5">XFORML</a> structure. This parameter can be <b>NULL</b>.


## -returns



If an error occurs, the return value is DDI_ERROR. Otherwise, the return value is a complexity hint about the transform object. The value of this transform characterization can be one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
Arbitrary 2 x 2 matrix and offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_IDENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identity matrix; no translation offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
Identity matrix; there is a translation offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_SCALE</b></dt>
</dl>
</td>
<td width="60%">
Off-diagonal matrix elements are zero.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5abfd19b-c946-45df-ae3b-b872ef706dd5">XFORML</a>



<a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a>



<a href="https://msdn.microsoft.com/a9267d2a-96ab-4518-8045-428ab74bd599">XFORMOBJ_bApplyXform</a>
 

 

