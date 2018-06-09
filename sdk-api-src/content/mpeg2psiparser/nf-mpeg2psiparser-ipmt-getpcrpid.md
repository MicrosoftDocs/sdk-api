---
UID: NF:mpeg2psiparser.IPMT.GetPcrPid
title: IPMT::GetPcrPid
author: windows-sdk-content
description: The GetPcrPid method returns the packet identifier (PID) of the packets that contain the Program Clock Reference (PCR) fields for this program.
old-location: mstv\ipmt_getpcrpid.htm
old-project: mstv
ms.assetid: 0099e5b3-d573-47b9-9581-fbb9fee3ca16
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetPcrPid, GetPcrPid method [Microsoft TV Technologies], GetPcrPid method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetPcrPid method, IPMT.GetPcrPid, IPMT::GetPcrPid, IPMTGetPcrPid, mpeg2psiparser/IPMT::GetPcrPid, mstv.ipmt_getpcrpid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetPcrPid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetPcrPid


## -description



The <b>GetPcrPid</b> method returns the packet identifier (PID) of the packets that contain the Program Clock Reference (PCR) fields for this program.




## -parameters




### -param pPidVal [out]

Receives the PCR_PID field.


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
 




## -see-also




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

