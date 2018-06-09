---
UID: NF:mpeg2psiparser.IPMT.QueryMPEInfo
title: IPMT::QueryMPEInfo
author: windows-sdk-content
description: The QueryMPEInfo method returns the multi-protocol encapsulation (MPE) information in the PMT, if any.
old-location: mstv\ipmt_querympeinfo.htm
old-project: mstv
ms.assetid: 14611397-7885-4553-905e-db56404f5e97
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],QueryMPEInfo method, IPMT.QueryMPEInfo, IPMT::QueryMPEInfo, IPMTQueryMPEInfo, QueryMPEInfo, QueryMPEInfo method [Microsoft TV Technologies], QueryMPEInfo method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::QueryMPEInfo, mstv.ipmt_querympeinfo
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
 - IPMT.QueryMPEInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::QueryMPEInfo


## -description



The <b>QueryMPEInfo</b> method returns the multi-protocol encapsulation (MPE) information in the PMT, if any.




## -parameters




### -param ppMPEList [out]

Address of a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/2753160b-de52-4d62-960a-c200c6f5f29a">MPE_ELEMENT</a> structures. The client must free the array by calling the <b>CoTaskMemFree</b> function.


### -param puiCount [out]

Receives the number of elements returned in <i>ppMPEList</i>.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
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
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
Malformed table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MPE_INFO_FOUND</b></dt>
</dl>
</td>
<td width="60%">
MPE information was found in the PMT.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MPE_INFO_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
MPE information was not found in the PMT.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, it returns one of the two success codes listed in the previous table. It returns MPEG2_S_MPE_INFO_FOUND if the PMT contains MPE information, or MPEG2_S_MPE_INFO_NOT_FOUND if the PMT does not contain any MPE information.




## -see-also




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

