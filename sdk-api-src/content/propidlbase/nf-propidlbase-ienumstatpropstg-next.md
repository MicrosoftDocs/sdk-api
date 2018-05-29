---
UID: NF:propidlbase.IEnumSTATPROPSTG.Next
title: IEnumSTATPROPSTG::Next
author: windows-sdk-content
description: Retrieves a specified number of STATPROPSTG structures, that follow subsequently in the enumeration sequence.
old-location: stg\ienumstatpropstg_next.htm
old-project: Stg
ms.assetid: 8e911da9-0056-4267-b9d0-c4ba929ddb94
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IEnumSTATPROPSTG interface [Structured Storage],Next method, IEnumSTATPROPSTG.Next, IEnumSTATPROPSTG::Next, Next, Next method [Structured Storage], Next method [Structured Storage],IEnumSTATPROPSTG interface, propidlbase/IEnumSTATPROPSTG::Next, stg.ienumstatpropstg_next
ms.prod: windows
ms.technology: windows-sdk
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
-	IEnumSTATPROPSTG.Next
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumSTATPROPSTG::Next


## -description


The <b>Next</b> method retrieves a specified number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures, that follow subsequently in the enumeration sequence. If fewer than the requested number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures exist in the enumeration sequence, it retrieves the remaining <b>STATPROPSTG</b> structures.


## -parameters




### -param celt [in]

The number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures requested.


### -param rgelt [out]

An array of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures returned.


### -param pceltFetched [out]

The number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures  retrieved in the <i>rgelt</i> parameter.


## -returns



This method supports the following return values.

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
The number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures returned is equal to the number specified in the <i>celt</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of <a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a> structures returned is less than the number specified in the <i>celt</i> parameter.

</td>
</tr>
</table>
 



