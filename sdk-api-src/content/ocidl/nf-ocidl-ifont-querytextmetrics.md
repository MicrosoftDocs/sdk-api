---
UID: NF:ocidl.IFont.QueryTextMetrics
title: IFont::QueryTextMetrics
author: windows-sdk-content
description: Fills a caller-allocated structure with information about the font.
old-location: com\ifont_querytextmetrics.htm
old-project: com
ms.assetid: 960dcc0b-8769-415c-9d5a-eaf9f4b3aeac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFont interface [COM],QueryTextMetrics method, IFont.QueryTextMetrics, IFont::QueryTextMetrics, QueryTextMetrics, QueryTextMetrics method [COM], QueryTextMetrics method [COM],IFont interface, _ctrl_ifont_querytextmetrics, com.ifont_querytextmetrics, ocidl/IFont::QueryTextMetrics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.QueryTextMetrics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IFont::QueryTextMetrics


## -description


Fills a caller-allocated structure with information about the font. 


## -parameters




### -param pTM [out]

Pointer to the caller-allocated structure that receives the font information. The 
   <b>TEXTMETRICOLE</b> structure is defined as a 
   <a href="https://msdn.microsoft.com/0a46da58-5d0f-4db4-bba6-9e1b6c1f892c">TEXTMETRICW</a> structure.


## -returns



The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the 
      following values.

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
The text metrics were returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>ptm</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<b>E_NOTIMPL</b> is not a valid return value. Font objects must always provide their font 
     information through this call unless other errors occur.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>
 

 

