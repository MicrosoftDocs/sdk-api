---
UID: NF:atscpsipparser.ICaptionServiceDescriptor.GetWideAspectRatio
title: ICaptionServiceDescriptor::GetWideAspectRatio
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icaptionservicedescriptor_getwideaspectratio.htm
old-project: mstv
ms.assetid: 921d919a-5e23-4c09-abff-3ed1e7dbec01
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetWideAspectRatio, GetWideAspectRatio method [Microsoft TV Technologies], GetWideAspectRatio method [Microsoft TV Technologies],ICaptionServiceDescriptor interface, ICaptionServiceDescriptor interface [Microsoft TV Technologies],GetWideAspectRatio method, ICaptionServiceDescriptor.GetWideAspectRatio, ICaptionServiceDescriptor::GetWideAspectRatio, ICaptionServiceDescriptorGetWideAspectRatio, atscpsipparser/ICaptionServiceDescriptor::GetWideAspectRatio, mstv.icaptionservicedescriptor_getwideaspectratio
ms.prod: windows
ms.technology: windows-sdk
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
-	ICaptionServiceDescriptor.GetWideAspectRatio
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICaptionServiceDescriptor::GetWideAspectRatio


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetWideAspectRatio</b> method queries whether a caption service is formatted for wide-screen displays.


## -parameters




### -param bIndex [in]

Zero-based index of the caption service. To get the number of caption services, call <a href="https://msdn.microsoft.com/50c2baff-a355-45a4-8a05-a193e695c448">ICaptionServiceDescriptor::GetNumberOfServices</a>.


### -param pbVal [out]

Receives the wide_aspect_ratio:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The caption service is formatted for a 4:3 aspect ratio.</td>
</tr>
<tr>
<td>1</td>
<td>The caption service is formatted for a 16:9 aspect ratio.</td>
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
 

 

