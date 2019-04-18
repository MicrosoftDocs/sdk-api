---
UID: NN:bits5_0.IBackgroundCopyJob5
title: IBackgroundCopyJob5 (bits5_0.h)
author: windows-sdk-content
description: Use this interface to query or set several optional behaviors of a job.
old-location: bits\bits5_functions.htm
tech.root: Bits
ms.assetid: 97481F9D-1F7B-473A-B288-A52E527478A0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob5, IBackgroundCopyJob5 interface [BITS], IBackgroundCopyJob5 interface [BITS],described, bits.bits5_functions, bits.ibackgroundcopyjob5, bits5_0/IBackgroundCopyJob5
ms.topic: interface
req.header: bits5_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits5_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: Bitsprx7.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bitsprx7.dll
api_name:
 - IBackgroundCopyJob5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBackgroundCopyJob5 interface


## -description


Use this interface to query or set several optional behaviors of a job.

To get this interface, call the <b>IBackgroundCopyJob::QueryInterface</b> method using 
    <code>__uuidof(IBackgroundCopyJob5)</code> as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyJob5</b> interface inherits from <a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>, <a href="https://msdn.microsoft.com/9fd422ba-a68c-40e3-8b21-3077b271e58e">IBackgroundCopyJob2</a>, <a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>, and <a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob4</a>. <b>IBackgroundCopyJob5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyJob5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/567C21C7-C689-4A13-9DCA-D45766CB5150">GetProperty</a>
</td>
<td align="left" width="63%">
A generic method for getting BITS job properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D5DB8A96-7417-4142-BA27-783314835CED">SetProperty</a>
</td>
<td align="left" width="63%">
A generic method for setting BITS job properties.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a>



<a href="https://msdn.microsoft.com/9fd422ba-a68c-40e3-8b21-3077b271e58e">IBackgroundCopyJob2</a>



<a href="https://msdn.microsoft.com/46e115bb-2634-4b79-b307-45720d8cb2be">IBackgroundCopyJob3</a>



<a href="https://msdn.microsoft.com/68909710-f749-487e-b064-9f8630929c53">IBackgroundCopyJob4</a>
 

 

