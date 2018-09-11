---
UID: NF:oleauto.SafeArrayGetVartype
title: SafeArrayGetVartype function
author: windows-sdk-content
description: Gets the VARTYPE stored in the specified safe array.
old-location: automat\safearraygetvartype.htm
tech.root: automat
ms.assetid: 8ec0e736-bac8-4df4-ba32-433cd8478c55
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SafeArrayGetVartype, SafeArrayGetVartype function [Automation], _oa96_SafeArrayGetVartype, automat.safearraygetvartype, oleauto/SafeArrayGetVartype
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayGetVartype
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayGetVartype function


## -description


Gets the VARTYPE stored in the specified safe array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.



### -param pvt [out]

The VARTYPE.


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
One of the arguments is not valid.

</td>
</tr>
</table>
 




## -remarks



If FADF_HAVEVARTYPE is set, <b>SafeArrayGetVartype</b> returns the VARTYPE stored in the array descriptor. If FADF_RECORD is set, it returns VT_RECORD; if FADF_DISPATCH is set, it returns VT_DISPATCH; and if FADF_UNKNOWN is set, it returns VT_UNKNOWN.

<b>SafeArrayGetVartype</b> can fail to return VT_UNKNOWN for SAFEARRAY types that are based on <b>IUnknown</b>. Callers should additionally check whether the SAFEARRAY type's <b>fFeatures</b> field has the FADF_UNKNOWN flag set. 




## -see-also




<a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY Data Type</a>
 

 

