---
UID: NF:mpeg2psiparser.IPAT.RegisterForNextTable
title: IPAT::RegisterForNextTable method
author: windows-driver-content
description: The RegisterForNextTable method registers the client to be notified when a next table arrives that will replace the current table.
old-location: mstv\ipat_registerfornexttable.htm
old-project: mstv
ms.assetid: 347d8c6f-0934-4ea0-9914-9b4ac47a9306
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IPAT, IPAT interface [Microsoft TV Technologies], RegisterForNextTable method, IPAT::RegisterForNextTable, IPATRegisterForNextTable, RegisterForNextTable method [Microsoft TV Technologies], RegisterForNextTable method [Microsoft TV Technologies], IPAT interface, RegisterForNextTable,IPAT.RegisterForNextTable, mpeg2psiparser/IPAT::RegisterForNextTable, mstv.ipat_registerfornexttable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpeg2psiparser.h
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
-	Mpeg2PsiParser.h
api_name:
-	IPAT.RegisterForNextTable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::RegisterForNextTable method


## -description



The <b>RegisterForNextTable</b> method registers the client to be notified when a <i>next</i> table arrives that will replace the current table.




## -parameters




### -param hNextTableAvailable [in]

Handle to an event created by the caller. The object signals the event when the <i>next</i> table arrives. When the event is signaled, call the <a href="https://msdn.microsoft.com/24cc3c97-60f6-440d-80fd-da7516698a2e">IPAT::GetNextTable</a> method to retrieve the table.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This table is already a <i>next</i> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>hNextTableAvailable</i> cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The method has already been called.

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



This method applies only to <i>current</i> tables. Otherwise, the method returns E_ACCESSDENIED.




## -see-also




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

