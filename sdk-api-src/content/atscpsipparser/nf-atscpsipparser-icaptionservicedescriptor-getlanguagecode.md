---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetLanguageCode
title: ICaptionServiceDescriptor::GetLanguageCode
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icaptionservicedescriptor_getlanguagecode.htm
tech.root: mstv
ms.assetid: 4b3b31dd-83cc-4067-a46f-929e1a75087a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLanguageCode, GetLanguageCode method [Microsoft TV Technologies], GetLanguageCode method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetLanguageCode method, ICaptionServiceDescriptor.GetLanguageCode, ICaptionServiceDescriptor::GetLanguageCode, ICaptionServiceDescriptorGetLanguageCode, atscpsipparser/ICaptionServiceDescriptor::GetLanguageCode, mstv.icaptionservicedescriptor_getlanguagecode
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - ICaptionServiceDescriptor.GetLanguageCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICaptionServiceDescriptor::GetLanguageCode


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetLanguageCode</b> method returns the language code for a specified caption service.


## -parameters




### -param bIndex [in]

Zero-based index of the caption service. To get the number of caption services, call <a href="https://msdn.microsoft.com/50c2baff-a355-45a4-8a05-a193e695c448">ICaptionServiceDescriptor::GetNumberOfServices</a>.


### -param LangCode [out]

Address of a 3-byte array that receives the ISO-639 language code.


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
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_INCORRECT_DESCRIPTOR_TAG</b></dt>
</dl>
</td>
<td width="60%">
The table descriptor tag is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The PSIP table is not well formed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>bIndex</i> parameter is out of range.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fc1f38af-2fe8-4c08-b6f8-312dd4771141">ICaptionServiceDescriptor Interface</a>
 

 

