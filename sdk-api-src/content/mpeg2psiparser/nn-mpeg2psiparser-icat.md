---
UID: NN:mpeg2psiparser.ICAT
title: ICAT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icat.htm
old-project: mstv
ms.assetid: 00da2af8-0f1a-467a-b310-8b8c7e564013
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: ICAT, ICAT interface [Microsoft TV Technologies], ICAT interface [Microsoft TV Technologies],described, ICATInterface, mpeg2psiparser/ICAT, mstv.icat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mpeg2psiparser.h
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mpeg2psiparser.h
api_name:
 - ICAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ICAT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>ICAT</b> interface enables the client to get data from a conditional access table (CAT). The <a href="https://msdn.microsoft.com/9da30d7d-4536-4753-9687-b2c16b560f2d">IAtscPsipParser::GetCAT</a> method returns a pointer to this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICAT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICAT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICAT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdd8f7a6-0c77-4058-bcca-9d712da781e0">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3111eecc-b869-4235-8af4-cc0ef9cc5e4e">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors in the CAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/466643d5-02d1-4ac1-9143-867f503aad09">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ff5a4dd-e332-4995-84a3-abfbbda087f9">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table descriptor for the CAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f28fb2c1-d9bb-4786-b3cc-db9583752e1b">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the CAT for a descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d117e4dd-5e7f-4f60-b657-25eae0f655cc">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the CAT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17d77207-253f-48e2-a7ec-3bcc549d2d5e">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74a5c410-314e-4f49-b294-a4788e85cbef">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

