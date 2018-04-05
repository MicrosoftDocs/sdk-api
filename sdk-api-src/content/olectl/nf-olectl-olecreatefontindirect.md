---
UID: NF:olectl.OleCreateFontIndirect
title: OleCreateFontIndirect function
author: windows-driver-content
description: Creates and initializes a standard font object using an initial description of the font's properties in a FONTDESC structure.
old-location: com\olecreatefontindirect.htm
old-project: com
ms.assetid: 9ab384d6-fc21-4152-a0cf-744948f2f72c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: OleCreateFontIndirect, OleCreateFontIndirect function [COM], _ole_OleCreateFontIndirect, com.olecreatefontindirect, olectl/OleCreateFontIndirect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PARAMDATA, *LPPARAMDATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	OleCreateFontIndirect
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# OleCreateFontIndirect function


## -description


Creates and initializes a standard font object using an initial description of the font's properties in a <a href="https://msdn.microsoft.com/c677b0ba-fd52-40e8-b7c3-b80a01c9fb26">FONTDESC</a> structure. The function returns an interface pointer to the new font object specified by caller in the riid parameter. A <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> call is part of this call. The caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> through the interface pointer returned.




## -parameters




### -param lpFontDesc [in]

Address of a caller-allocated, <a href="https://msdn.microsoft.com/c677b0ba-fd52-40e8-b7c3-b80a01c9fb26">FONTDESC</a> structure containing the initial state of the font. This value must not be <b>NULL</b>.


### -param riid [in]

Reference to the identifier of the interface describing the type of interface pointer to return in <i>lplpvObj</i>.


### -param lplpvObj [out]

 Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, this parameter contains the requested interface pointer on the newly created font object. If successful, the caller is responsible to call Release through this interface pointer when the new object is no longer needed. If unsuccessful, the value of is set to <b>NULL</b>.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provided interface identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pFontDesc</i> or <i>ppvObj</i> is not valid. Note that if <i>pFontDesc</i> is set to <b>NULL</b>, the function returns NO_ERROR.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c677b0ba-fd52-40e8-b7c3-b80a01c9fb26">FONTDESC</a>
 

 

