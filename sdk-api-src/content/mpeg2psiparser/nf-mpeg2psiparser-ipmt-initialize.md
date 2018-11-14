---
UID: NF:mpeg2psiparser.IPMT.Initialize
title: IPMT::Initialize
author: windows-sdk-content
description: The Initialize method initializes the object using captured table section data. This method is called internally by the IAtscPsipParser::GetPMT method, so applications typically should not call it.
old-location: mstv\ipmt_initialize.htm
tech.root: MSTV
ms.assetid: d9f5e6b0-4317-40cd-9664-e2cc6d1a8833
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],Initialize method, IPMT.Initialize, IPMT::Initialize, IPMTInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::Initialize, mstv.ipmt_initialize
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
 - IPMT.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mpeg2psiparser.h
: 
- IPMT.Initialize
: 
---

# IPMT::Initialize


## -description



The <b>Initialize</b> method initializes the object using captured table section data. This method is called internally by the <a href="https://msdn.microsoft.com/cd9a3fb0-4bdc-499b-9db9-85dce50dd24b">IAtscPsipParser::GetPMT</a> method, so applications typically should not call it.




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




<a href="https://msdn.microsoft.com/0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24">IPMT Interface</a>
 

 

