---
UID: NF:mpeg2psiparser.IPMT.GetTableDescriptorByIndex
title: IPMT::GetTableDescriptorByIndex
author: windows-sdk-content
description: The GetTableDescriptorByIndex method retrieves a table-wide descriptor for the PMT.
old-location: mstv\ipmt_gettabledescriptorbyindex.htm
old-project: mstv
ms.assetid: 31442c1f-0921-49b8-ab38-d75ccc2c4f0e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IPMT interface, IPMT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IPMT.GetTableDescriptorByIndex, IPMT::GetTableDescriptorByIndex, IPMTGetTableDescriptorByIndex, mpeg2psiparser/IPMT::GetTableDescriptorByIndex, mstv.ipmt_gettabledescriptorbyindex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2psiparser.h
req.include-header: 
req.redist: 
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
 - IPMT.GetTableDescriptorByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT::GetTableDescriptorByIndex


## -description



The <b>GetTableDescriptorByIndex</b> method retrieves a table-wide descriptor for the PMT.




## -parameters




### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/e1f91a13-afec-4703-8f1c-be64c8a8b8f9">IPMT::GetCountOfTableDescriptors</a> method to get the number of table descriptors in the PMT.


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
 

 

