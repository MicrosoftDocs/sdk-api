---
UID: NF:mpeg2psiparser.IPMT.GetRecordDescriptorByIndex
title: IPMT::GetRecordDescriptorByIndex (mpeg2psiparser.h)
author: windows-sdk-content
description: The GetRecordDescriptorByIndex method retrieves a descriptor for a specified record in the PMT.
old-location: mstv\ipmt_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: 1e37db4b-1b86-4b34-8f93-642bb603789e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IPMT.GetRecordDescriptorByIndex, IPMT::GetRecordDescriptorByIndex, IPMTGetRecordDescriptorByIndex, mpeg2psiparser/IPMT::GetRecordDescriptorByIndex, mstv.ipmt_getrecorddescriptorbyindex
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IPMT::GetRecordDescriptorByIndex


## -description



The <b>GetRecordDescriptorByIndex</b> method retrieves a descriptor for a specified record in the PMT.




## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694822(v=VS.85).aspx">IPMT::GetCountOfRecords</a> method to get the number of records in the PMT.


### -param dwDescIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/en-us/library/Dd694827(v=VS.85).aspx">IPMT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd694820(v=VS.85).aspx">IPMT Interface</a>
 

 

