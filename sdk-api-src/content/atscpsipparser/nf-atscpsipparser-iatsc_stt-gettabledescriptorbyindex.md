---
UID: NF:atscpsipparser.IATSC_STT.GetTableDescriptorByIndex
title: IATSC_STT::GetTableDescriptorByIndex
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_stt_gettabledescriptorbyindex.htm
old-project: mstv
ms.assetid: 9f48ad31-ec6b-4d82-ba74-9901281a1857
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IATSC_STT.GetTableDescriptorByIndex, IATSC_STT::GetTableDescriptorByIndex, IATSC_STTGetTableDescriptorByIndex, atscpsipparser/IATSC_STT::GetTableDescriptorByIndex, mstv.iatsc_stt_gettabledescriptorbyindex
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_STT.GetTableDescriptorByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_STT::GetTableDescriptorByIndex


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTableDescriptorByIndex</b> method returns a descriptor for the STT.


## -parameters




### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="https://msdn.microsoft.com/527e64b4-c280-46d6-8579-a5755d4b242c">IATSC_STT::GetCountOfTableDescriptors</a> method to get the number of table descriptors in the STT.


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




<a href="https://msdn.microsoft.com/03e903e0-e722-42c6-b6b7-448fecc379b9">IATSC_STT Interface</a>
 

 

