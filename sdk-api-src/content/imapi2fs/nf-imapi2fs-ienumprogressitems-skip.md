---
UID: NF:imapi2fs.IEnumProgressItems.Skip
title: IEnumProgressItems::Skip
author: windows-sdk-content
description: Skips a specified number of items in the enumeration sequence.
old-location: imapi\ienumprogressitems_skip.htm
tech.root: imapi
ms.assetid: 789b2003-1538-4617-a44b-38b80320e21c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnumProgressItems interface [IMAPI],Skip method, IEnumProgressItems.Skip, IEnumProgressItems::Skip, Skip, Skip method [IMAPI], Skip method [IMAPI],IEnumProgressItems interface, imapi.ienumprogressitems_skip, imapi2fs/IEnumProgressItems::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - IEnumProgressItems.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumProgressItems::Skip


## -description


Skips a specified number of items in the enumeration sequence.


## -parameters




### -param celt [in]

Number of items to skip. 


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>
 




## -remarks



If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.





## -see-also




<a href="https://msdn.microsoft.com/c4238fbe-762a-492f-9eb5-d927e64436e1">IEnumProgressItems</a>
 

 

