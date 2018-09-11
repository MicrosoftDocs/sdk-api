---
UID: NF:mpeg2psiparser.IPAT.GetVersionNumber
title: IPAT::GetVersionNumber
author: windows-sdk-content
description: The GetVersionNumber method returns the version number for the PAT.
old-location: mstv\ipat_getversionnumber.htm
tech.root: mstv
ms.assetid: 1398a1b9-e9b9-4f30-ba93-0a08a0994cf9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetVersionNumber method, IPAT.GetVersionNumber, IPAT::GetVersionNumber, IPATGetVersionNumber, mpeg2psiparser/IPAT::GetVersionNumber, mstv.ipat_getversionnumber
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
 - IPAT.GetVersionNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPAT::GetVersionNumber


## -description



The <b>GetVersionNumber</b> method returns the version number for the PAT.




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




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

