---
UID: NF:dvbsiparser.IDVB_TOT.GetCountOfTableDescriptors
title: IDVB_TOT::GetCountOfTableDescriptors (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_tot_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: 1c043aa8-683b-4770-81cb-3d3e9c35342f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IDVB_TOT interface, IDVB_TOT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IDVB_TOT.GetCountOfTableDescriptors, IDVB_TOT::GetCountOfTableDescriptors, IDVB_TOTGetCountOfTableDescriptors, dvbsiparser/IDVB_TOT::GetCountOfTableDescriptors, mstv.idvb_tot_getcountoftabledescriptors
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDVB_TOT.GetCountOfTableDescriptors"
req.header: dvbsiparser.h
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
 - dvbsiparser.h
api_name:
 - IDVB_TOT.GetCountOfTableDescriptors
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_TOT::GetCountOfTableDescriptors


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfTableDescriptors</b> method returns the number of descriptors in the TOT.


## -parameters




### -param pdwVal [out]

Pointer to a variable that receives the number of descriptors.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_tot">IDVB_TOT Interface</a>
 

 

