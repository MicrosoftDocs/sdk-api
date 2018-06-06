---
UID: NF:wmcodecdsp.IWMCodecStrings.GetName
title: IWMCodecStrings::GetName
author: windows-sdk-content
description: Retrieves the name of a codec.
old-location: mf\iwmcodecstringsgetname.htm
old-project: medfound
ms.assetid: 12422e46-dfde-4a0f-8988-567a42f5a212
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetName, GetName method [Media Foundation], GetName method [Media Foundation],IWMCodecStrings interface, IWMCodecStrings interface [Media Foundation],GetName method, IWMCodecStrings.GetName, IWMCodecStrings::GetName, codecapi.iwmcodecstringsgetname, mf.iwmcodecstringsgetname, wmcodecdsp/ IWMCodecStrings::GetName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMCodecStrings.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMCodecStrings::GetName


## -description



Retrieves the name of a codec.



## -parameters




### -param pmt [in]

Pointer to the output media type. If <b>NULL</b>, the codec will use the media type that is currently set.


### -param cchLength [in]

Size of szName buffer in wide characters.


### -param szName [out]

Address of the wide-character buffer that receives the name. If <b>NULL</b>, pcchLength receives the required length.


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
 

 

