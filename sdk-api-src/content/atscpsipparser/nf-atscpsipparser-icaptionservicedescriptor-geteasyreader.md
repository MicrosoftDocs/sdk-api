---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetEasyReader
title: ICaptionServiceDescriptor::GetEasyReader
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icaptionservicedescriptor_geteasyreader.htm
tech.root: MSTV
ms.assetid: 7ecf31c8-b93e-4c6c-991c-33ce942757ec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetEasyReader, GetEasyReader method [Microsoft TV Technologies], GetEasyReader method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetEasyReader method, ICaptionServiceDescriptor.GetEasyReader, ICaptionServiceDescriptor::GetEasyReader, ICaptionServiceDescriptorGetEasyReader, atscpsipparser/ICaptionServiceDescriptor::GetEasyReader, mstv.icaptionservicedescriptor_geteasyreader
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
 - ICaptionServiceDescriptor.GetEasyReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- atscpsipparser.h
: 
- ICaptionServiceDescriptor.GetEasyReader
: 
---

# ICaptionServiceDescriptor::GetEasyReader


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetEasyReader</b> method queries whether a caption service contains "Easy Reader" captions.


## -parameters




### -param bIndex [in]

Zero-based index of the caption service. To get the number of caption services, call <a href="https://msdn.microsoft.com/50c2baff-a355-45a4-8a05-a193e695c448">ICaptionServiceDescriptor::GetNumberOfServices</a>.


### -param pbVal [out]

Receives the easy_reader flag:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The caption service does not contain "Easy Reader" captions.</td>
</tr>
<tr>
<td>1</td>
<td>The caption service contains "Easy Reader" captions.</td>
</tr>
</table>
 


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
 

 

