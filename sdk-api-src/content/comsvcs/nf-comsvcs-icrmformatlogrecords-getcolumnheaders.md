---
UID: NF:comsvcs.ICrmFormatLogRecords.GetColumnHeaders
title: ICrmFormatLogRecords::GetColumnHeaders method
author: windows-driver-content
description: Retrieves the names of the fields (columns) so that they can be used as column headings when the information is presented.
old-location: cos\icrmformatlogrecords_getcolumnheaders.htm
old-project: cossdk
ms.assetid: b7ca50f9-7e42-4cde-9985-0501ae34f040
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetColumnHeaders method [COM+], GetColumnHeaders method [COM+], ICrmFormatLogRecords interface, GetColumnHeaders,ICrmFormatLogRecords.GetColumnHeaders, ICrmFormatLogRecords, ICrmFormatLogRecords interface [COM+], GetColumnHeaders method, ICrmFormatLogRecords::GetColumnHeaders, _dtc_ICrmFormatLogRecords_GetColumnHeaders, comsvcs/ICrmFormatLogRecords::GetColumnHeaders, cos.icrmformatlogrecords_getcolumnheaders
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICrmFormatLogRecords.GetColumnHeaders
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmFormatLogRecords::GetColumnHeaders method


## -description


Retrieves the names of the fields (columns) so that they can be used as column headings when the information is presented.


## -parameters




### -param pHeaders [out]

A <b>Variant</b> array containing the field names as <b>Variant</b> strings.



## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aa801bd0-5253-4f9f-8859-b808d4dc081b">ICrmFormatLogRecords</a>
 

 

