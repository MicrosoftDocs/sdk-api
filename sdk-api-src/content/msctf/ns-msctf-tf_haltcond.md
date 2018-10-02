---
UID: NS:msctf.TF_HALTCOND
title: TF_HALTCOND
author: windows-sdk-content
description: The TF_HALTCOND structure is used to contain conditions of a range shift.
old-location: tsf\tf_haltcond.htm
tech.root: TSF
ms.assetid: 055f3228-1e3b-4e31-9035-e509a98016a8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: TF_HALTCOND, TF_HALTCOND structure [Text Services Framework], _tsf_tf_haltcond_ref, msctf/TF_HALTCOND, tsf.tf_haltcond
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msctf.h
api_name:
 - TF_HALTCOND
product: Windows
targetos: Windows
req.typenames: TF_HALTCOND
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TF_HALTCOND structure


## -description



The <b>TF_HALTCOND</b> structure is used to contain conditions of a range shift.




## -struct-fields




### -field pHaltRange

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that halts the shift. If the range shift encounters this range during the shift, the shift halts. This member can be <b>NULL</b>.


### -field aHaltPos

Contains one of the <a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor</a> values that specifies which anchor of <b>pHaltRange</b> the anchor will get shifted to if <b>pHaltRange</b> is encountered during the range shift. This member is ignored if <b>pHaltRange</b> is <b>NULL</b>.


### -field dwFlags

Contains a set of flags that modify the behavior of the range shift. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TF_HF_OBJECT</td>
<td>The range shift halts if an embedded object is encountered.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="https://msdn.microsoft.com/1debec6d-f98f-45a4-aaa8-99b61f3583ef">ITfRange::ShiftEnd
      </a>



<a href="https://msdn.microsoft.com/f9f983b1-a5fa-4857-b73c-b879c566d6f6">ITfRange::ShiftStart
      </a>



<a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor
      </a>
 

 

