---
UID: NF:dvbsiparser.IDVB_BAT.GetRecordDescriptorByIndex
title: IDVB_BAT::GetRecordDescriptorByIndex
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_bat_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: ea1ace90-4378-4dec-9326-70e6f9814dde
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IDVB_BAT interface, IDVB_BAT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IDVB_BAT.GetRecordDescriptorByIndex, IDVB_BAT::GetRecordDescriptorByIndex, IDVB_BATGetRecordDescriptorByIndex, dvbsiparser/IDVB_BAT::GetRecordDescriptorByIndex, mstv.idvb_bat_getrecorddescriptorbyindex
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDVB_BAT.GetRecordDescriptorByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IDVB_BAT.GetRecordDescriptorByIndex
: 
---

# IDVB_BAT::GetRecordDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the BAT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/feb31eca-d746-48cf-8c1b-06dd7816725b">IDVB_BAT::GetCountOfRecords</a> method to get the number of records in the BAT.


### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/d3ef02f2-a593-4439-a460-e2b5fcd0ef70">IDVB_BAT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


### -param ppDescriptor [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/c312a152-21ee-4708-90a8-ab9bde9a2011">IDVB_BAT Interface</a>
 

 

