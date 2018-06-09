---
UID: NF:mpeg2psiparser.IPMT.GetRecordDescriptorByIndex
title: IPMT::GetRecordDescriptorByIndex
author: windows-sdk-content
description: The GetRecordDescriptorByIndex method retrieves a descriptor for a specified record in the PMT.
old-location: mstv\ipmt_getrecorddescriptorbyindex.htm
old-project: mstv
ms.assetid: 1e37db4b-1b86-4b34-8f93-642bb603789e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IPMT.GetRecordDescriptorByIndex, IPMT::GetRecordDescriptorByIndex, IPMTGetRecordDescriptorByIndex, mpeg2psiparser/IPMT::GetRecordDescriptorByIndex, mstv.ipmt_getrecorddescriptorbyindex
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
 - IPMT.GetRecordDescriptorByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetRecordDescriptorByIndex


## -description



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the PMT.




## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/f4e5009b-4c0d-4d0c-b480-4030cedbdb97">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.


### -param dwDescIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/b2470267-25a6-4ed3-91a1-30fd3ac7bbea">IPMT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


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




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

