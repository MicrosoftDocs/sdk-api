---
UID: NF:tapi3if.IEnumPluggableTerminalClassInfo.Skip
title: IEnumPluggableTerminalClassInfo::Skip
author: windows-sdk-content
description: The Skip method skips over the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.
old-location: tapi3\ienumpluggableterminalclassinfo_skip.htm
tech.root: tapi
ms.assetid: 19880df4-7c1c-4840-a1c9-c51f2e9fd0fc
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IEnumPluggableTerminalClassInfo interface [TAPI 2.2],Skip method, IEnumPluggableTerminalClassInfo.Skip, IEnumPluggableTerminalClassInfo::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumPluggableTerminalClassInfo interface, _tapi3_ienumpluggableterminalclassinfo_skip, tapi3.ienumpluggableterminalclassinfo_skip, tapi3if/IEnumPluggableTerminalClassInfo::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumPluggableTerminalClassInfo.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPluggableTerminalClassInfo::Skip


## -description


The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.


## -parameters




### -param celt [in]

Number of elements to skip.


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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/72c0db41-8391-4923-8961-6aefce9886c4">IEnumPluggableTerminalClassInfo</a>



<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">Terminal Class</a>
 

 

