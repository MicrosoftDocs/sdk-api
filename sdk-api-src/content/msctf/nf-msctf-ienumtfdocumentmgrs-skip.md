---
UID: NF:msctf.IEnumTfDocumentMgrs.Skip
title: IEnumTfDocumentMgrs::Skip
author: windows-driver-content
description: IEnumTfDocumentMgrs::Skip method
old-location: tsf\ienumtfdocumentmgrs_skip.htm
old-project: TSF
ms.assetid: 04464160-d171-4c83-91f0-068a1c13544a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IEnumTfDocumentMgrs interface [Text Services Framework],Skip method, IEnumTfDocumentMgrs.Skip, IEnumTfDocumentMgrs::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfDocumentMgrs interface, _tsf_ienumtfdocumentmgrs_skip_ref, msctf/IEnumTfDocumentMgrs::Skip, tsf.ienumtfdocumentmgrs_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	IEnumTfDocumentMgrs.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfDocumentMgrs::Skip


## -description




## -parameters




### -param ulCount [in]

Contains the number of elements to skip.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>
 



