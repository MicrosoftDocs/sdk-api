---
UID: NF:atscpsipparser.ISCTE_EAS.Initialize
title: ISCTE_EAS::Initialize method
author: windows-driver-content
description: The Initialize method initializes the object using captured table section data. This method is called internally by the IAtscPsipParser::GetEAS method, so applications typically should not call it.
old-location: mstv\iscte_eas_initialize.htm
old-project: mstv
ms.assetid: f40e89f4-6a33-44a9-933c-bf38978f1cb2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], Initialize method, ISCTE_EAS::Initialize, ISCTE_EASInitialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies], ISCTE_EAS interface, Initialize,ISCTE_EAS.Initialize, atscpsipparser/ISCTE_EAS::Initialize, mstv.iscte_eas_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
-	ISCTE_EAS.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISCTE_EAS::Initialize method


## -description



      The <b>Initialize</b> method initializes the object using captured table section data. This method is called internally by the <a href="https://msdn.microsoft.com/e53b93e3-7269-45aa-8b19-75f78fb44c41">IAtscPsipParser::GetEAS</a> method, so applications typically should not call it.


## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface.


### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the <a href="https://msdn.microsoft.com/03027748-03da-485c-8787-3cf171fff1e0">MPEG-2 Sections and Tables</a> filter.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
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
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The EAS table is not well formed.

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




<a href="https://msdn.microsoft.com/7b5620c3-f460-4118-a8a2-9b2561bd12cf">ISCTE_EAS Interface</a>
 

 

