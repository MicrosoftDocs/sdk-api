---
UID: NF:imapi2.IDiscFormat2Data.get_MultisessionInterfaces
title: IDiscFormat2Data::get_MultisessionInterfaces
author: windows-sdk-content
description: Retrieves a list of available multi-session interfaces.
old-location: imapi\idiscformat2data_get_multisessioninterfaces.htm
tech.root: imapi
ms.assetid: 7bb2d100-629f-4b63-a699-ddce85213e72
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_MultisessionInterfaces method, IDiscFormat2Data.get_MultisessionInterfaces, IDiscFormat2Data::get_MultisessionInterfaces, get_MultisessionInterfaces, get_MultisessionInterfaces method [IMAPI], get_MultisessionInterfaces method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_multisessioninterfaces, imapi2/IDiscFormat2Data::get_MultisessionInterfaces
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDiscFormat2Data.get_MultisessionInterfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2Data::get_MultisessionInterfaces


## -description


Retrieves a list of available multi-session interfaces.


## -parameters




### -param value [out]

List of available multi-session interfaces. Each element of the array is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for any interface that inherits from <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a> interface, for example, <a href="https://msdn.microsoft.com/b8124597-e75a-4f95-a25c-8cf59f452548">IMultisessionSequential</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  This method does not return an error when called on blank optical media.</div>
<div> </div>



## -remarks



The array will always contain at least one element.




## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>
 

 

