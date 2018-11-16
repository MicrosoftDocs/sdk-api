---
UID: NN:wmcodecdsp.ITocParser
title: ITocParser
author: windows-sdk-content
description: The ITocParser interface represents a TOC Parser object. It provides methods for storing tables of contents in a video file and retrieving tables of contents from a video file.
old-location: mf\itocparser.htm
tech.root: medfound
ms.assetid: d1f14a6e-d75c-4266-beff-0e9af911edfe
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITocParser, ITocParser interface [Media Foundation], ITocParser interface [Media Foundation],described, codecapi.itocparser, mf.itocparser, wmcodecdsp/ITocParser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - ITocParser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITocParser interface


## -description


The <b>ITocParser</b> interface represents a TOC Parser object. It provides methods for storing tables of contents in a video file and retrieving tables of contents from a video file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocParser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITocParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c99ccbb3-ba33-4d87-81a3-0de3c180554a">AddToc</a>
</td>
<td align="left" width="63%">
Adds a table of contents to the TOC Parser object and assigns an index to the added table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/549c170e-2e4d-4edb-b84e-178bfbb13fed">Commit</a>
</td>
<td align="left" width="63%">
Stores the current state of the TOC Parser object in its associated media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1386e348-c94f-4343-908c-338352eae494">GetTocByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table of contents, specified by an index, from the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97a3b835-5d99-4b37-8f1d-2469e85faf9b">GetTocByType</a>
</td>
<td align="left" width="63%">
Retrieves all tables of contents of a specified type from the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ad80a20-cadb-4a0d-a39e-b627324df425">GetTocCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of tables of contents, of a specified <a href="https://msdn.microsoft.com/cc2fbadc-43f7-470c-873b-de2dc9d84e5d">position type</a>, in the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d7a9bda-56e8-4b42-ace5-4d6cf5d52b59">Init</a>
</td>
<td align="left" width="63%">
 Initializes the TOC Parser object and associates it with a media file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ec459bf-c631-4ad4-beb3-4cd1e89c1d35">RemoveTocByIndex</a>
</td>
<td align="left" width="63%">
Removes a table of contents, specified by an index, from the TOC Parser object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3d32dc9-ccae-46fd-9dd4-62e300981da0">RemoveTocByType</a>
</td>
<td align="left" width="63%">
Removes all tables of contents of a specified type from the TOC Parser object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/25039e6c-dd2a-4516-bf27-8e9d6ca0f00e">Table of Contents Parser Interfaces</a>
 

 

