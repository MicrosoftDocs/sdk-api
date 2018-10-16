---
UID: NF:wmcodecdsp.ITocParser.GetTocByIndex
title: ITocParser::GetTocByIndex
author: windows-sdk-content
description: The GetTocByIndex method retrieves a table of contents, specified by an index, from the TOC Parser object.
old-location: mf\itocparser_gettocbyindex.htm
tech.root: medfound
ms.assetid: 1386e348-c94f-4343-908c-338352eae494
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetTocByIndex, GetTocByIndex method [Media Foundation], GetTocByIndex method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],GetTocByIndex method, ITocParser.GetTocByIndex, ITocParser::GetTocByIndex, codecapi.itocparser_gettocbyindex, mf.itocparser_gettocbyindex, wmcodecdsp/ITocParser::GetTocByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocParser.GetTocByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocParser::GetTocByIndex


## -description


The <b>GetTocByIndex</b> method retrieves a table of contents, specified by an index, from the TOC Parser object.


## -parameters




### -param arg1

TBD


### -param dwTocIndex [in]

The index of the table of contents to be retrieved.


### -param ppToc [out]

Pointer to a variable that receives a pointer to an <a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a> interface that represents the retrieved table of contents.


#### - enumTocPosType [in]

A member of the <a href="https://msdn.microsoft.com/799059b5-9949-48af-8c54-4cb4975f8249">TOC_POS_TYPE</a> enumeration that specifies the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of the table of contents to be retrieved.


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




<a href="https://msdn.microsoft.com/d1f14a6e-d75c-4266-beff-0e9af911edfe">ITocParser Interface</a>
 

 

