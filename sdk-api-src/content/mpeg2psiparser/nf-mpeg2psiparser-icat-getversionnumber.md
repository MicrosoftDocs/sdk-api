---
UID: NF:mpeg2psiparser.ICAT.GetVersionNumber
title: ICAT::GetVersionNumber method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icat_getversionnumber.htm
old-project: mstv
ms.assetid: d117e4dd-5e7f-4f60-b657-25eae0f655cc
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies], ICAT interface, GetVersionNumber,ICAT.GetVersionNumber, ICAT, ICAT interface [Microsoft TV Technologies], GetVersionNumber method, ICAT::GetVersionNumber, ICATGetVersionNumber, mpeg2psiparser/ICAT::GetVersionNumber, mstv.icat_getversionnumber
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
-	mpeg2psiparser.h
api_name:
-	ICAT.GetVersionNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ICAT::GetVersionNumber method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetVersionNumber</b> method returns the version number for the CAT.


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




<a href="https://msdn.microsoft.com/00da2af8-0f1a-467a-b310-8b8c7e564013">ICAT Interface</a>
 

 

