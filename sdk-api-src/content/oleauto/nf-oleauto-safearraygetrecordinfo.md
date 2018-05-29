---
UID: NF:oleauto.SafeArrayGetRecordInfo
title: SafeArrayGetRecordInfo function
author: windows-sdk-content
description: Retrieves the IRecordInfo interface of the UDT contained in the specified safe array.
old-location: automat\safearraygetrecordinfo.htm
old-project: automat
ms.assetid: 1584c00e-06a5-44f4-8c4b-a2b23737a652
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayGetRecordInfo, SafeArrayGetRecordInfo function [Automation], _oa96_SafeArrayGetRecordInfo, automat.safearraygetrecordinfo, oleauto/SafeArrayGetRecordInfo
ms.prod: windows
ms.technology: windows-sdk
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
-	SafeArrayGetRecordInfo
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SafeArrayGetRecordInfo function


## -description


Retrieves the <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a> interface of the UDT contained in the specified safe array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.



### -param prinfo [out]

The <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a> interface.


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
The argument <i>psa</i> is null or the array descriptor does not have the FADF_RECORD flag set.

</td>
</tr>
</table>
 



