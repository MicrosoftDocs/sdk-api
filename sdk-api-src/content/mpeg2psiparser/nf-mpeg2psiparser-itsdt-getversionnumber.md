---
UID: NF:mpeg2psiparser.ITSDT.GetVersionNumber
title: ITSDT::GetVersionNumber
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itsdt_getversionnumber.htm
old-project: mstv
ms.assetid: 4784b7d6-1a20-4018-9ad5-7e8bafb700f8
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],ITSDT interface, ITSDT interface [Microsoft TV Technologies],GetVersionNumber method, ITSDT.GetVersionNumber, ITSDT::GetVersionNumber, ITSDTGetVersionNumber, mpeg2psiparser/ITSDT::GetVersionNumber, mstv.itsdt_getversionnumber
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
-	ITSDT.GetVersionNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ITSDT::GetVersionNumber


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetVersionNumber</b> method returns the version number for the TSDT.


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




<a href="https://msdn.microsoft.com/58ec73dc-79bd-415b-b9be-8e9246166391">ITSDT Interface</a>
 

 

