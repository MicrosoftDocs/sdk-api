---
UID: NF:dvbsiparser.IDVB_TOT.GetTableDescriptorByIndex
title: IDVB_TOT::GetTableDescriptorByIndex (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_tot_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: 0d59b778-c8bc-4ccc-bca2-013c2345814f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IDVB_TOT interface, IDVB_TOT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IDVB_TOT.GetTableDescriptorByIndex, IDVB_TOT::GetTableDescriptorByIndex, IDVB_TOTGetTableDescriptorByIndex, dvbsiparser/IDVB_TOT::GetTableDescriptorByIndex, mstv.idvb_tot_gettabledescriptorbyindex
ms.topic: method
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
 - IDVB_TOT.GetTableDescriptorByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_TOT::GetTableDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTableDescriptorByIndex</b> method retrieves a descriptor for the TOT.


## -parameters




### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/1c043aa8-683b-4770-81cb-3d3e9c35342f">IDVB_TOT::GetCountOfTableDescriptors</a> method to get the number of table descriptors in the TOT.


### -param ppDescriptor [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd694093(v=VS.85).aspx">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

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




<a href="https://msdn.microsoft.com/fe5b6b7c-fc6b-4889-b780-4b9f61f3e895">IDVB_TOT Interface</a>
 

 

