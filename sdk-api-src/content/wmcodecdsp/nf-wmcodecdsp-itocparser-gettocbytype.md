---
UID: NF:wmcodecdsp.ITocParser.GetTocByType
title: ITocParser::GetTocByType
author: windows-sdk-content
description: The GetTocByType retrieves all tables of contents of a specified type from the TOC Parser object.
old-location: mf\itocparser_gettocbytype.htm
tech.root: medfound
ms.assetid: 97a3b835-5d99-4b37-8f1d-2469e85faf9b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTocByType, GetTocByType method [Media Foundation], GetTocByType method [Media Foundation],ITocParser interface, ITocParser interface [Media Foundation],GetTocByType method, ITocParser.GetTocByType, ITocParser::GetTocByType, codecapi.itocparser_gettocbytype, mf.itocparser_gettocbytype, wmcodecdsp/ITocParser::GetTocByType
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
 - ITocParser.GetTocByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocParser::GetTocByType


## -description


The <b>GetTocByType</b> retrieves all tables of contents of a specified type from the TOC Parser object.


## -parameters




### -param arg1 [in]

A member of the <a href="https://msdn.microsoft.com/799059b5-9949-48af-8c54-4cb4975f8249">TOC_POS_TYPE</a> enumeration that specifies the <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a> of the table of contents to be retrieved.


### -param guidTocType [in]

A globally unique identifier (<b>GUID</b>) that specifies the type of table of contents to retrieve. See Remarks.


### -param ppTocs [out]

Pointer to an <a href="https://msdn.microsoft.com/10d6fc04-4444-4a47-911f-3d5bec548e28">ITocCollection</a> interface that represents the colleciton of retrieved tables of contents.


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
 




## -remarks



You might want to design several different type of tables of contents. In that case, you can distinguish between types by creating a <b>GUID</b> that represents each type. You can identify a table of contents as a particular type by setting the <b>guidType</b> member of a <a href="https://msdn.microsoft.com/a79f75c5-be98-4120-85be-71bedbcc0ea2">TOC_DESCRIPTOR</a> structure and then passing the <b>TOC_DESCRIPTOR</b> structure to <a href="https://msdn.microsoft.com/55208226-fd2d-48e5-887b-34e95309a770">IToc::SetDescriptor</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1f14a6e-d75c-4266-beff-0e9af911edfe">ITocParser</a>



<a href="https://msdn.microsoft.com/e3d32dc9-ccae-46fd-9dd4-62e300981da0">RemoveTocByType</a>
 

 

