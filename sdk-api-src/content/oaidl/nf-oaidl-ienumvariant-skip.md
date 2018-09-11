---
UID: NF:oaidl.IEnumVARIANT.Skip
title: IEnumVARIANT::Skip
author: windows-sdk-content
description: Attempts to skip over the next celt elements in the enumeration sequence.
old-location: automat\ienumvariant_skip.htm
tech.root: automat
ms.assetid: 5fe6951f-1e21-4a3d-8694-96efb15e6d11
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumVARIANT interface [Automation],Skip method, IEnumVARIANT.Skip, IEnumVARIANT::Skip, Skip, Skip method [Automation], Skip method [Automation],IEnumVARIANT interface, _oa96_IEnumVARIANT::Skip, automat.ienumvariant_skip, oaidl/IEnumVARIANT::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - COM
api_location:
 - oaidl.h
api_name:
 - IEnumVARIANT.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumVARIANT::Skip


## -description


Attempts to skip over the next celt elements in the enumeration sequence.


## -parameters




### -param celt [in]

The number of elements to skip.



## -returns



This method can return one of these values.

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
The specified number of elements was skipped.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The end of the sequence was reached before skipping the requested number of elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>
 

 

