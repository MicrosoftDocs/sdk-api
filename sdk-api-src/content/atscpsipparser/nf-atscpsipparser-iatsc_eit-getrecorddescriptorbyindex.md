---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordDescriptorByIndex
title: IATSC_EIT::GetRecordDescriptorByIndex
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_eit_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: 06144d3d-b789-4ba3-b313-958de366764f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IATSC_EIT.GetRecordDescriptorByIndex, IATSC_EIT::GetRecordDescriptorByIndex, IATSC_EITGetRecordDescriptorByIndex, atscpsipparser/IATSC_EIT::GetRecordDescriptorByIndex, mstv.iatsc_eit_getrecorddescriptorbyindex
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_EIT.GetRecordDescriptorByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_EIT::GetRecordDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method returns a descriptor for a specified record in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/edf16862-5bc4-4022-9727-11c1a291417d">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.


### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/fd568711-c82c-4ffe-9333-2b729502fe79">IATSC_EIT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


### -param ppDescriptor [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


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




<a href="https://msdn.microsoft.com/ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6">IATSC_EIT Interface</a>
 

 

