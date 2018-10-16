---
UID: NF:wmcodecdsp.ITocParser.GetTocCount
title: ITocParser::GetTocCount
author: windows-sdk-content
description: The GetTocCount method retrieves the number of tables of contents, of a specified position type, in the TOC Parser object.
old-location: mf\itocparser_gettoccount.htm
tech.root: medfound
ms.assetid: 8ad80a20-cadb-4a0d-a39e-b627324df425
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetTocCount, GetTocCount method [Media Foundation], GetTocCount method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],GetTocCount method, ITocParser.GetTocCount, ITocParser::GetTocCount, codecapi.itocparser_gettoccount, mf.itocparser_gettoccount, wmcodecdsp/ITocParser::GetTocCount
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
 - ITocParser.GetTocCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocParser::GetTocCount


## -description


The <b>GetTocCount</b> method retrieves the number of tables of contents, of a specified <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a>, in the TOC Parser object.


## -parameters




### -param arg1

TBD


### -param pdwTocCount [out]

Pointer to a <b>DWORD</b> that receives the number of tables of contents.


#### - enumTocPosType [in]

A member of the <a href="https://msdn.microsoft.com/799059b5-9949-48af-8c54-4cb4975f8249">TOC_POS_TYPE</a> enumeration that specifies the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of the tables of contents to be counted.


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
 

 

