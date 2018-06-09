---
UID: NF:dvbsiparser.IDVB_NIT.GetRecordDescriptorByIndex
title: IDVB_NIT::GetRecordDescriptorByIndex
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_nit_getrecorddescriptorbyindex.htm
old-project: mstv
ms.assetid: b81651b1-2b70-4012-b219-57d495724033
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IDVB_NIT interface, IDVB_NIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IDVB_NIT.GetRecordDescriptorByIndex, IDVB_NIT::GetRecordDescriptorByIndex, IDVB_NITGetRecordDescriptorByIndex, dvbsiparser/IDVB_NIT::GetRecordDescriptorByIndex, mstv.idvb_nit_getrecorddescriptorbyindex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_NIT.GetRecordDescriptorByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_NIT::GetRecordDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the NIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/fb0f8071-575a-4bbd-b34b-b8d92c17c476">IDVB_NIT::GetCountOfRecords</a> method to get the number of records in the NIT.


### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/3f3e43d8-5063-4fac-bbec-22b6876716f0">IDVB_NIT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


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




<a href="https://msdn.microsoft.com/70b638ae-0152-4a44-aeb1-f3ac382c19ce">IDVB_NIT Interface</a>
 

 

