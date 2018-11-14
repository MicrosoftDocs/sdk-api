---
UID: NF:mergemod.IMsmMerge.ExtractCAB
title: IMsmMerge::ExtractCAB
author: windows-sdk-content
description: The ExtractCAB method extracts the embedded .cab file from a module and saves it as the specified file.
old-location: setup\imsmmerge_extractcab.htm
tech.root: msi
ms.assetid: 3f794dac-6eeb-4c1e-8c23-c9d7384f650f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ExtractCAB, ExtractCAB method, ExtractCAB method,IMsmMerge interface, IMsmMerge interface,ExtractCAB method, IMsmMerge.ExtractCAB, IMsmMerge::ExtractCAB, _msi_extractcab_function, mergemod/IMsmMerge::ExtractCAB, setup.imsmmerge_extractcab
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.ExtractCAB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mergemod.h
: 
- IMsmMerge.ExtractCAB
: 
---

# IMsmMerge::ExtractCAB


## -description


The 
<b>ExtractCAB</b> method extracts the embedded .cab file from a module and saves it as the specified file. The installer creates this file if it does not already exist and overwrites the file if it does exist. For more information, see the 
<a href="https://msdn.microsoft.com/a6fe8b69-8f4a-45f7-b7e6-7620a00500bb">ExtractCAB</a> method of the 
<a href="https://msdn.microsoft.com/3f76ee8a-d195-4a69-99a3-31ef2c1c72d5">Merge</a> object.  

<b>IMsmMerge2::ExtractCAB</b>    Mergemod.dll version 2.0 or later.<div> </div><b>IMsmMerge::ExtractCAB</b>      All Mergemod.dll versions.
			
			


## -parameters




### -param FileName [in]

The fully qualified destination file. A <b>LPCWSTR</b> may be used in place of a <b>BSTR</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not create the output file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_FAULT as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
Could not write data to the output file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to access embedded .cab file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No embedded .cab file was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

