---
UID: NF:wmcontainer.IMFASFStreamPrioritization.GetStreamCount
title: IMFASFStreamPrioritization::GetStreamCount
author: windows-sdk-content
description: Note  This interface is not implemented in this version of Media Foundation. Retrieves the number of entries in the stream priority list.
old-location: mf\imfasfstreamprioritization_getstreamcount.htm
old-project: medfound
ms.assetid: 8c9dacbb-a952-411e-82df-0c8768d0b3fe
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 8c9dacbb-a952-411e-82df-0c8768d0b3fe, GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFASFStreamPrioritization interface, IMFASFStreamPrioritization interface [Media Foundation],GetStreamCount method, IMFASFStreamPrioritization.GetStreamCount, IMFASFStreamPrioritization::GetStreamCount, mf.imfasfstreamprioritization_getstreamcount, wmcontainer/IMFASFStreamPrioritization::GetStreamCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSINK_WMDRMACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamPrioritization.GetStreamCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IMFASFStreamPrioritization::GetStreamCount


## -description



<div class="alert"><b>Note</b>  This interface is not implemented in this version of Media Foundation.</div>
<div> </div>
Retrieves the number of entries in the stream priority list.




## -parameters




### -param pdwStreamCount






#### - dwStreamIndex [out]

Receives the number of streams in the stream priority list.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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




<a href="https://msdn.microsoft.com/6eb79c52-dc81-406c-9000-d25ad380e6b2">IMFASFStreamPrioritization</a>
 

 

