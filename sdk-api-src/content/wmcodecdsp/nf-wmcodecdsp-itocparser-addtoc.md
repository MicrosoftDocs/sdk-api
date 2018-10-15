---
UID: NF:wmcodecdsp.ITocParser.AddToc
title: ITocParser::AddToc
author: windows-sdk-content
description: The AddToc method adds a table of contents to the TOC Parser object and assigns an index to the added table of contents.
old-location: mf\itocparser_addtoc.htm
tech.root: medfound
ms.assetid: c99ccbb3-ba33-4d87-81a3-0de3c180554a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AddToc, AddToc method [Media Foundation], AddToc method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],AddToc method, ITocParser.AddToc, ITocParser::AddToc, codecapi.itocparser_addtoc, mf.itocparser_addtoc, wmcodecdsp/ITocParser::AddToc
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
 - ITocParser.AddToc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocParser::AddToc


## -description


The <b>AddToc</b> method adds a table of contents to the TOC Parser object and assigns an index to the added table of contents.


## -parameters




### -param arg1

TBD


### -param pToc [in]

Pointer to an <a href="https://msdn.microsoft.com/b12d38c7-b80e-4ca8-9ac5-a116100911d0">IToc</a> interface that represents the table of contents to be added.


### -param pdwTocIndex [out]

Pointer to a <b>DWORD</b> that receives the index of the added table of contents.


#### - enumTocPosType [in]

A member of the <a href="https://msdn.microsoft.com/799059b5-9949-48af-8c54-4cb4975f8249">TOC_POS_TYPE</a> enumeration that specifies the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of the table of contents to be added.


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




<a href="https://msdn.microsoft.com/1386e348-c94f-4343-908c-338352eae494">GetTocByIndex</a>



<a href="https://msdn.microsoft.com/d1f14a6e-d75c-4266-beff-0e9af911edfe">ITocParser</a>
 

 

