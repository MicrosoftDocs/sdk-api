---
UID: NF:imapi2.IStreamPseudoRandomBased.get_ExtendedSeed
title: IStreamPseudoRandomBased::get_ExtendedSeed (imapi2.h)
author: windows-sdk-content
description: Retrieves an array of seed values used by the random number generator.
old-location: imapi\istreampseudorandombased_get_extendedseed.htm
tech.root: imapi
ms.assetid: e15e47aa-e5c4-4944-a3c4-14e459a31bb5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStreamPseudoRandomBased interface [IMAPI],get_ExtendedSeed method, IStreamPseudoRandomBased.get_ExtendedSeed, IStreamPseudoRandomBased::get_ExtendedSeed, get_ExtendedSeed, get_ExtendedSeed method [IMAPI], get_ExtendedSeed method [IMAPI],IStreamPseudoRandomBased interface, imapi.istreampseudorandombased_get_extendedseed, imapi2/IStreamPseudoRandomBased::get_ExtendedSeed
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IStreamPseudoRandomBased.get_ExtendedSeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamPseudoRandomBased::get_ExtendedSeed


## -description


Retrieves an array of seed values used by the random number generator.


## -parameters




### -param values [out]

Array of seed values used by the random number generator.


### -param eCount [out]

Number of seed values in the <i>values</i> array.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7630b8ac-41f9-4cc7-95e7-4172a876673f">IStreamPseudoRandomBased</a>



<a href="https://msdn.microsoft.com/c5362760-84c6-4e93-b3cd-2ce568b13102">IStreamPseudoRandomBased::get_Seed</a>



<a href="https://msdn.microsoft.com/a6edf21f-b89a-4780-8065-4d09758fe701">IStreamPseudoRandomBased::put_ExtendedSeed</a>
 

 

