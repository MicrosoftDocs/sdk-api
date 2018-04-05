---
UID: NF:atscpsipparser.IATSC_VCT.GetCountOfTableDescriptors
title: IATSC_VCT::GetCountOfTableDescriptors method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_getcountoftabledescriptors.htm
old-project: mstv
ms.assetid: 6930490f-235f-40d5-846d-ae9a075c82cc
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies], IATSC_VCT interface, GetCountOfTableDescriptors,IATSC_VCT.GetCountOfTableDescriptors, IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], GetCountOfTableDescriptors method, IATSC_VCT::GetCountOfTableDescriptors, IATSC_VCTGetCountOfTableDescriptors, atscpsipparser/IATSC_VCT::GetCountOfTableDescriptors, mstv.iatsc_vct_getcountoftabledescriptors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
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
req.typenames: APPX_PACKAGE_WRITER_PAYLOAD_STREAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_VCT.GetCountOfTableDescriptors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_VCT::GetCountOfTableDescriptors method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of table-wide descriptors in the VCT.


## -parameters




### -param pdwVal [in]

Receives the number of descriptors.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

