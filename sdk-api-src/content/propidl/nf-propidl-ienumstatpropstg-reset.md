---
UID: NF:propidl.IEnumSTATPROPSTG.Reset
title: IEnumSTATPROPSTG::Reset
author: windows-driver-content
description: Resets the enumeration sequence to the beginning of the STATPROPSTG structure array.
old-location: stg\ienumstatpropstg_reset.htm
old-project: Stg
ms.assetid: e742e3ee-6261-4d6d-85ca-8df770aa58ad
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IEnumSTATPROPSTG interface [Structured Storage],Reset method, IEnumSTATPROPSTG.Reset, IEnumSTATPROPSTG::Reset, Reset, Reset method [Structured Storage], Reset method [Structured Storage],IEnumSTATPROPSTG interface, propidlbase/IEnumSTATPROPSTG::Reset, stg.ienumstatpropstg_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propidl.h
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
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IEnumSTATPROPSTG.Reset
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumSTATPROPSTG::Reset


## -description


The <b>Reset</b> method resets the enumeration sequence to the beginning of the <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structure array.


## -parameters






## -returns



This method supports the S_OK return value.

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
The enumeration sequence was successfully reset to the beginning of the enumeration.

</td>
</tr>
</table>
 



