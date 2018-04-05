---
UID: NF:mpeg2psiparser.IPAT.Initialize
title: IPAT::Initialize method
author: windows-driver-content
description: The Initialize method initializes the object using captured table section data. This method is called internally by the IAtscPsipParser::GetPAT method, so applications typically should not call it.
old-location: mstv\ipat_initialize.htm
old-project: mstv
ms.assetid: 51aa6d14-655c-4800-87f0-85d9a77b6c15
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IPAT, IPAT interface [Microsoft TV Technologies], Initialize method, IPAT::Initialize, IPATInitialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies], IPAT interface, Initialize,IPAT.Initialize, mpeg2psiparser/IPAT::Initialize, mstv.ipat_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2PsiParser.h
api_name:
-	IPAT.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::Initialize method


## -description



The <b>Initialize</b> method initializes the object using captured table section data. This method is called internally by the <a href="https://msdn.microsoft.com/7cfa9ec0-a802-4dbe-9997-d0eaac2b71c9">IAtscPsipParser::GetPAT</a> method, so applications typically should not call it.




## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList</a> interface of the <b>SectionList</b> object that contains the section data.


### -param pMPEGData [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


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
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object is already initialized.

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




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

