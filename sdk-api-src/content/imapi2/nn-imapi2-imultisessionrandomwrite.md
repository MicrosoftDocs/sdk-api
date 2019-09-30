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
f1_keywords: 
 - "imapi2/IMultisessionRandomWrite"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMultisessionRandomWrite interface


## -description


Use this interface to retrieve information about the current state of media allowing random writes and not supporting the concept of physical sessions.

The following methods return a collection of <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a> interfaces representing all supported multisession types. 
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">IDiscFormat2Data::get_MultisessionInterfaces</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces">IFileSystemImage::get_MultisessionInterfaces</a>
</li>
</ul>


You can then call the IUnknown::QueryInterface method on each element in the collection to query for the <b>IMultisessionRandomWrite</b> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMultisessionRandomWrite</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>. <b>IMultisessionRandomWrite</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisessionrandomwrite-get_lastwrittenaddress">get_LastWrittenAddress</a>
</td>
<td align="left" width="63%">
Retrieves the last written address on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisessionrandomwrite-get_totalsectorsonmedia">get_TotalSectorsOnMedia</a>
</td>
<td align="left" width="63%">
Retrieves the total number of sectors on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-imultisessionrandomwrite-get_writeunitsize">get_WriteUnitSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of a writeable unit on the media.

</td>
</tr>
</table> 


## -remarks



If more than one multi-session interface exist, the application can let <a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a> choose a compatible multi-session interface to use or the application can specify the multi-session interface to use by setting the <i>put_InUse</i> property to <b>VARIANT_TRUE</b>.

A file system creator would use the address properties to import the content of the previous session on the disc and to compute the position of the next session it will create. These properties will return the same values as the properties of the same name of the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a> interface.
This is a <b>MsftMultisessionRandomWrite</b> object in script.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_multisessioninterfaces">IDiscFormat2Data::get_MultisessionInterfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces">IFileSystemImage::get_MultisessionInterfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>
 

 

