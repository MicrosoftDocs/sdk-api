---
UID: NF:dvbsiparser.IDVB_SDT.GetRecordDescriptorByIndex
title: IDVB_SDT::GetRecordDescriptorByIndex (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: acf392b4-519b-4bcc-b0e4-8d5a72442aa5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IDVB_SDT.GetRecordDescriptorByIndex, IDVB_SDT::GetRecordDescriptorByIndex, IDVB_SDTGetRecordDescriptorByIndex, dvbsiparser/IDVB_SDT::GetRecordDescriptorByIndex, mstv.idvb_sdt_getrecorddescriptorbyindex
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
 - IDVB_SDT.GetRecordDescriptorByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_SDT::GetRecordDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the SDT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="https://msdn.microsoft.com/9815ba89-d5c2-4d13-8ed1-478953836bc7">IDVB_SDT::GetCountOfRecords</a> to get the number of records in the SDT.


### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/99b7e2ab-c829-4e42-805b-e1ea5b725f82">IDVB_SDT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


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




<a href="https://msdn.microsoft.com/bb473a7e-8957-4e85-98d0-13c6992fbf37">IDVB_SDT Interface</a>
 

 

