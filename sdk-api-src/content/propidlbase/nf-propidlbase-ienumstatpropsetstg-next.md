---
UID: NF:propidlbase.IEnumSTATPROPSETSTG.Next
title: IEnumSTATPROPSETSTG::Next
author: windows-driver-content
description: Retrieves a specified number of STATPROPSETSTG structures that follow subsequently in the enumeration sequence.
old-location: stg\ienumstatpropsetstg_next.htm
old-project: Stg
ms.assetid: 3af3c518-3db4-4436-b1c1-86587ce8fbf3
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IEnumSTATPROPSETSTG interface [Structured Storage],Next method, IEnumSTATPROPSETSTG.Next, IEnumSTATPROPSETSTG::Next, Next, Next method [Structured Storage], Next method [Structured Storage],IEnumSTATPROPSETSTG interface, propidlbase/IEnumSTATPROPSETSTG::Next, stg.ienumstatpropsetstg_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propidlbase.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STATPROPSTG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IEnumSTATPROPSETSTG.Next
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumSTATPROPSETSTG::Next


## -description


The <b>Next</b> method retrieves a specified number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures that follow subsequently in the enumeration sequence. If fewer than the requested number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures exist in the enumeration sequence, it retrieves the remaining <b>STATPROPSETSTG</b> structures.


## -parameters




### -param celt [in]

The number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures requested.


### -param rgelt [out]

An array of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures returned.


### -param pceltFetched [out]

The number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures  retrieved in the <i>rgelt</i> parameter.


## -returns



This method supports the following return values:

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
The number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures returned equals the number specified in the <i>celt</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of <a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a> structures returned is less than the number specified in the <i>celt</i> parameter.

</td>
</tr>
</table>
 



