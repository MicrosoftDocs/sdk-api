---
UID: NN:imapi2.IMultisessionRandomWrite
title: IMultisessionRandomWrite (imapi2.h)
author: windows-sdk-content
description: Use this interface to retrieve information about the current state of media allowing random writes and not supporting the concept of physical sessions.
old-location: imapi\imultisessionrandomwrite.htm
tech.root: imapi
ms.assetid: 1843254d-7947-4197-9c1b-6dc01abe9354
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMultisessionRandomWrite, IMultisessionRandomWrite interface [IMAPI], IMultisessionRandomWrite interface [IMAPI],described, imapi.imultisessionrandomwrite, imapi2/IMultisessionRandomWrite
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IMultisessionRandomWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMultisessionRandomWrite interface


## -description


Use this interface to retrieve information about the current state of media allowing random writes and not supporting the concept of physical sessions.

The following methods return a collection of <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a> interfaces representing all supported multisession types. 
<ul>
<li>
<a href="https://msdn.microsoft.com/7bb2d100-629f-4b63-a699-ddce85213e72">IDiscFormat2Data::get_MultisessionInterfaces</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10c0b02e-965e-47ca-95f4-237c21b505ad">IFileSystemImage::get_MultisessionInterfaces</a>
</li>
</ul>


You can then call the IUnknown::QueryInterface method on each element in the collection to query for the <b>IMultisessionRandomWrite</b> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultisessionRandomWrite</b> interface inherits from <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>. <b>IMultisessionRandomWrite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMultisessionRandomWrite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04d5c8ad-347c-4f2d-aa3d-3db77067a51e">get_LastWrittenAddress</a>
</td>
<td align="left" width="63%">
Retrieves the last written address on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22afe893-dc8b-42dc-bbb5-78ed245d300b">get_TotalSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the total number of sectors on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcf9f0ab-4095-4ff3-a72a-656ef74f04b8">get_WriteUnitSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of a writeable unit on the media.

</td>
</tr>
</table> 


## -remarks



If more than one multi-session interface exist, the application can let <a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a> choose a compatible multi-session interface to use or the application can specify the multi-session interface to use by setting the <i>put_InUse</i> property to <b>VARIANT_TRUE</b>.

A file system creator would use the address properties to import the content of the previous session on the disc and to compute the position of the next session it will create. These properties will return the same values as the properties of the same name of the <a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a> interface.
This is a <b>MsftMultisessionRandomWrite</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/7bb2d100-629f-4b63-a699-ddce85213e72">IDiscFormat2Data::get_MultisessionInterfaces</a>



<a href="https://msdn.microsoft.com/10c0b02e-965e-47ca-95f4-237c21b505ad">IFileSystemImage::get_MultisessionInterfaces</a>



<a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>
 

 

