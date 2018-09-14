---
UID: NF:mfidl.MFGetSupportedSchemes
title: MFGetSupportedSchemes function
author: windows-sdk-content
description: Retrieves the URL schemes that are registered for the source resolver.
old-location: mf\mfgetsupportedschemes.htm
tech.root: medfound
ms.assetid: b40315fc-7e2b-4573-a98f-840b6ce31dd3
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: MFGetSupportedSchemes, MFGetSupportedSchemes function [Media Foundation], b40315fc-7e2b-4573-a98f-840b6ce31dd3, mf.mfgetsupportedschemes, mfidl/MFGetSupportedSchemes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFGetSupportedSchemes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetSupportedSchemes function


## -description



Retrieves the URL schemes that are registered for the source resolver.




## -parameters




### -param pPropVarSchemeArray [out]

Pointer to a <b>PROPVARIANT</b> that receives the URL schemes. Before calling this method, call <b>PropVariantInit</b> to initialize the <b>PROPVARIANT</b>. If the method succeeds, the <b>PROPVARIANT</b> contains an array of wide-character strings. The <b>PROPVARIANT</b> data type is VT_VECTOR | VT_LPWSTR. The caller must release the <b>PROPVARIANT</b> by calling <b>PropVariantClear</b>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

