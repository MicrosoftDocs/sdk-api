---
UID: NF:msctf.IEnumTfUIElements.Skip
title: IEnumTfUIElements::Skip method
author: windows-driver-content
description: The IEnumTfUIElements::Skip method obtains, from the current position, the specified number of elements in the enumeration sequence.
old-location: tsf\ienumtfuielements_skip.htm
old-project: TSF
ms.assetid: 44ba8fb1-e702-4f53-b95a-719b4fdfcaa0
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEnumTfUIElements, IEnumTfUIElements interface [Text Services Framework], Skip method, IEnumTfUIElements::Skip, Skip method [Text Services Framework], Skip method [Text Services Framework], IEnumTfUIElements interface, Skip,IEnumTfUIElements.Skip, msctf/IEnumTfUIElements::Skip, tsf.ienumtfuielements_skip
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
-	Msctf.dll
api_name:
-	IEnumTfUIElements.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfUIElements::Skip method


## -description


The <b>IEnumTfUIElements::Skip</b> method obtains, from the current position, the specified number of elements in the enumeration sequence.


## -parameters




### -param ulCount [in]

[in] Specifies the number of elements to skip.


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
 



