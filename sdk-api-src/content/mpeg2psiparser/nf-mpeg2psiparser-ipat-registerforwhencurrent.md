---
UID: NF:mpeg2psiparser.IPAT.RegisterForWhenCurrent
title: IPAT::RegisterForWhenCurrent method
author: windows-driver-content
description: The RegisterForWhenCurrent method registers the client to be notified when the table becomes current.
old-location: mstv\ipat_registerforwhencurrent.htm
old-project: mstv
ms.assetid: 2a7808b6-2e31-4cd9-a4cc-7a6a7cf46cd4
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IPAT, IPAT interface [Microsoft TV Technologies], RegisterForWhenCurrent method, IPAT::RegisterForWhenCurrent, IPATRegisterForWhenCurrent, RegisterForWhenCurrent method [Microsoft TV Technologies], RegisterForWhenCurrent method [Microsoft TV Technologies], IPAT interface, RegisterForWhenCurrent,IPAT.RegisterForWhenCurrent, mpeg2psiparser/IPAT::RegisterForWhenCurrent, mstv.ipat_registerforwhencurrent
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
-	IPAT.RegisterForWhenCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::RegisterForWhenCurrent method


## -description



The <b>RegisterForWhenCurrent</b> method registers the client to be notified when the table becomes current.




## -parameters




### -param hNextTableIsCurrent [in]

Handle to an event created by the caller. The object signals the event when the table becomes current.


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
This table is already a <i>current</i> table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument; <i>hNextTableIsCurrent</i> cannot be <b>NULL</b>.

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



This method applies only to <i>next</i> tables. Otherwise, the method returns E_ACCESSDENIED.




## -see-also




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

