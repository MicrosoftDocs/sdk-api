---
UID: NF:oleauto.CreateErrorInfo
title: CreateErrorInfo function
author: windows-driver-content
description: Creates an instance of a generic error object.
old-location: automat\createerrorinfo.htm
old-project: automat
ms.assetid: 6a9dd862-754a-48e3-8be5-d1fbd1d38f2b
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: CreateErrorInfo, CreateErrorInfo function [Automation], _oa96_CreateErrorInfo, automat.createerrorinfo, oleauto/CreateErrorInfo
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
-	API-MS-Win-Downlevel-OLE32-l1-1-1.dll
-	ComBase.dll
api_name:
-	CreateErrorInfo
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CreateErrorInfo function


## -description


Creates an instance of a generic error object.


## -parameters




### -param pperrinfo [out]

A system-implemented generic error object.


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
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Could not create the error object.

</td>
</tr>
</table>
 




## -remarks



This function returns a pointer to a generic error object, which you can use with <b>QueryInterface</b> on <a href="https://msdn.microsoft.com/2e7c5ad5-9018-413e-8826-ef752ebf302c">ICreateErrorInfo</a> to set its contents. You can then pass the resulting object to <a href="8EAACFAC-FC37-4EAA-870B-10B99D598D66">SetErrorInfo</a>. The generic error object implements both <b>ICreateErrorInfo</b> and <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/483ca37a-332c-4a0e-9c27-cc6b885a3005">Error-Handling API Functions</a>
 

 

