---
UID: NF:wmcodecdsp.ITocParser.RemoveTocByIndex
title: ITocParser::RemoveTocByIndex
author: windows-sdk-content
description: The RemoveTocByIndex method removes a table of contents, specified by an index, from the TOC Parser object.
old-location: mf\itocparser_removetocbyindex.htm
old-project: medfound
ms.assetid: 7ec459bf-c631-4ad4-beb3-4cd1e89c1d35
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ITocParser interface [Media Foundation],RemoveTocByIndex method, ITocParser.RemoveTocByIndex, ITocParser::RemoveTocByIndex, RemoveTocByIndex, RemoveTocByIndex method [Media Foundation], RemoveTocByIndex method [Media Foundation],ITocParser interface, codecapi.itocparser_removetocbyindex, mf.itocparser_removetocbyindex, wmcodecdsp/ITocParser::RemoveTocByIndex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmcodecdsp.h
req.include-header: 
req.redist: 
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
 - ITocParser.RemoveTocByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocParser::RemoveTocByIndex


## -description


The <b>RemoveTocByIndex</b> method removes a table of contents, specified by an index, from the TOC Parser object.


## -parameters




### -param param




### -param dwTocIndex [in]

The index of the table of contents to be removed.


#### - enumTocPosType [in]

A member of the <a href="https://msdn.microsoft.com/799059b5-9949-48af-8c54-4cb4975f8249">TOC_POS_TYPE</a> enumeration that specifies the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of the table of contents to be removed.


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




<a href="https://msdn.microsoft.com/d1f14a6e-d75c-4266-beff-0e9af911edfe">ITocParser</a>
 

 

