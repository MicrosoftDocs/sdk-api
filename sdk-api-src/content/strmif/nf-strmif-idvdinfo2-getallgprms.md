---
UID: NF:strmif.IDvdInfo2.GetAllGPRMs
title: IDvdInfo2::GetAllGPRMs
author: windows-sdk-content
description: The GetAllGPRMs method retrieves the current contents of all general parameter registers (GPRMs).
old-location: dshow\idvdinfo2_getallgprms.htm
tech.root: DirectShow
ms.assetid: 994f57b5-8514-4768-a679-21133ec92e32
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetAllGPRMs, GetAllGPRMs method [DirectShow], GetAllGPRMs method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetAllGPRMs method, IDvdInfo2.GetAllGPRMs, IDvdInfo2::GetAllGPRMs, IDvdInfo2GetAllGPRMs, dshow.idvdinfo2_getallgprms, strmif/IDvdInfo2::GetAllGPRMs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetAllGPRMs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo2::GetAllGPRMs


## -description



The <b>GetAllGPRMs</b> method retrieves the current contents of all general parameter registers (GPRMs).




## -parameters




### -param pRegisterArray [out]

Pointer to an array of type <a href="https://msdn.microsoft.com/f0ab0a9d-00fa-4c61-9f5a-727cf69ffa1c">GPRMARRAY</a> that receives all 16 current GPRM values.
          


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



GPRMs are 16-bit registers that each disc can use in unique ways for temporary data storage. 

<div class="alert"><b>Note</b>  A player application using the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter does not need to access these registers for any Annex J playback or navigation control. This method is provided for player applications implementing advanced functionality. Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification, and the ways in which the GPRMs are used on the particular discs to be played.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

