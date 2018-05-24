---
UID: NF:wmcodecdsp.IToc.SetContext
title: IToc::SetContext
author: windows-driver-content
description: The SetContext method associates a caller-supplied context block with the table of contents.
old-location: mf\itoc_setcontext.htm
old-project: medfound
ms.assetid: 45aadac5-6c65-4525-a1fc-b045337a6030
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IToc interface [Media Foundation],SetContext method, IToc.SetContext, IToc::SetContext, SetContext, SetContext method [Media Foundation], SetContext method [Media Foundation],IToc interface, codecapi.itoc_setcontext, mf.itoc_setcontext, wmcodecdsp/IToc::SetContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFVideoDSPMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmvdspa.dll
api_name:
-	IToc.SetContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IToc::SetContext


## -description


The <b>SetContext</b> method associates a caller-supplied context block with the table of contents.


## -parameters




### -param dwContextSize [in]

The size, in bytes, of the context block.


### -param pbtContext [in]

Pointer to the first byte of the context block.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



You can use this method to associate any information with the table of contents. The type of information you store in the context block is completely up to you. TOC Parser does not inspect or interpret the context block.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545736">GetContext</a>



<a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a>
 

 

