---
UID: NF:wmcodecdsp.IWMCodecStrings.GetDescription
title: IWMCodecStrings::GetDescription method
author: windows-driver-content
description: Retrieves the description of an output format.
old-location: mf\iwmcodecstringsgetdescription.htm
old-project: medfound
ms.assetid: 79068e6c-bd16-45e4-a8af-6a03e0c5b528
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetDescription method [Media Foundation], GetDescription method [Media Foundation], IWMCodecStrings interface, GetDescription,IWMCodecStrings.GetDescription, IWMCodecStrings, IWMCodecStrings interface [Media Foundation], GetDescription method, IWMCodecStrings::GetDescription, codecapi.iwmcodecstringsgetdescription, mf.iwmcodecstringsgetdescription, wmcodecdsp/ IWMCodecStrings::GetDescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
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
req.typenames: MFVideoDSPMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmcodecdsp.h
api_name:
-	IWMCodecStrings.GetDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecStrings::GetDescription method


## -description



Retrieves the description of an output format.



## -parameters




### -param pmt [in]

Pointer to the output media type. If <b>NULL</b>, the codec will use the media type that is currently set.


### -param cchLength [in]

Size of szDescription buffer, in wide characters.


### -param szDescription [out]

Address of the wide-character buffer that receives the description. If <b>NULL</b>, pcchLength receives the required length.


### -param pcchLength [out]

Pointer to the required buffer length in wide characters, including the null terminating character.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84b6223e-d42a-47b0-8553-2b4d69de2da3">IWMCodecStrings Interface</a>
 

 

