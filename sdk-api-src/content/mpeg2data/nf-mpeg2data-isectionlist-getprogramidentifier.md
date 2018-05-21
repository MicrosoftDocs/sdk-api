---
UID: NF:mpeg2data.ISectionList.GetProgramIdentifier
title: ISectionList::GetProgramIdentifier
author: windows-driver-content
description: The GetProgramIdentifier method retrieves the program identifier (PID) of the packets that this object is receiving.
old-location: mstv\isectionlist_getprogramidentifier.htm
old-project: mstv
ms.assetid: 25a4bd3c-ef02-4685-8c83-06025ce4410c
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetProgramIdentifier, GetProgramIdentifier method [Microsoft TV Technologies], GetProgramIdentifier method [Microsoft TV Technologies],ISectionList interface, ISectionList interface [Microsoft TV Technologies],GetProgramIdentifier method, ISectionList.GetProgramIdentifier, ISectionList::GetProgramIdentifier, ISectionListGetProgramIdentifier, mpeg2data/ISectionList::GetProgramIdentifier, mstv.isectionlist_getprogramidentifier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2data.h
api_name:
-	ISectionList.GetProgramIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISectionList::GetProgramIdentifier


## -description



The <b>GetProgramIdentifier</b> method retrieves the program identifier (PID) of the packets that this object is receiving.




## -parameters




### -param pPid

Receives the PID.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
NULL pointer argument.

</td>
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



The PID value is set when the object is first initialized.




## -see-also




<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList Interface</a>
 

 

