---
UID: NF:wmcodecdsp.ITocEntry.SetTitle
title: ITocEntry::SetTitle
author: windows-sdk-content
description: The SetTitle method sets the title of the entry.
old-location: mf\itocentry_settitle.htm
old-project: medfound
ms.assetid: 24ab6c56-59ae-4fdf-b18e-75f616ee5a80
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITocEntry interface [Media Foundation],SetTitle method, ITocEntry.SetTitle, ITocEntry::SetTitle, SetTitle, SetTitle method [Media Foundation], SetTitle method [Media Foundation],ITocEntry interface, codecapi.itocentry_settitle, mf.itocentry_settitle, wmcodecdsp/ITocEntry::SetTitle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcodecdsp.h
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
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocEntry.SetTitle
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocEntry::SetTitle


## -description


The <b>SetTitle</b> method sets the title of the entry.


## -parameters




### -param pwszTitle [in]

Pointer to a NULL-terminated wide-character string that contains the title.


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




<a href="https://msdn.microsoft.com/d610e9e8-daa4-4d8c-a640-627b23afd316">GetTitle</a>



<a href="https://msdn.microsoft.com/82a1a390-50b1-4699-9baa-60cea322ce7c">ITocEntry</a>
 

 

