---
UID: NF:mpeg2psiparser.IPMT.GetVersionNumber
title: IPMT::GetVersionNumber
author: windows-sdk-content
description: The GetVersionNumber method returns the version number for the PMT.
old-location: mstv\ipmt_getversionnumber.htm
tech.root: mstv
ms.assetid: 00385ea4-27a9-47f4-91af-22fa82d83668
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetVersionNumber method, IPMT.GetVersionNumber, IPMT::GetVersionNumber, IPMTGetVersionNumber, mpeg2psiparser/IPMT::GetVersionNumber, mstv.ipmt_getversionnumber
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT.GetVersionNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPMT::GetVersionNumber


## -description



The <b>GetVersionNumber</b> method returns the version number for the PMT.




## -parameters




### -param pbVal [out]

Receives the version_number field.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd694820(v=VS.85).aspx">IPMT Interface</a>
 

 

