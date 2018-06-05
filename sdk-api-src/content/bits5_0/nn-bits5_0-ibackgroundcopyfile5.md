---
UID: NN:bits5_0.IBackgroundCopyFile5
title: IBackgroundCopyFile5
author: windows-sdk-content
description: Use this interface to get or set generic properties of BITS file transfers.
old-location: bits\ibackgroundcopyfile5.htm
old-project: Bits
ms.assetid: 548b507a-4874-4ccf-829e-13e1ca6cc958
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBackgroundCopyFile5, IBackgroundCopyFile5 interface [BITS], IBackgroundCopyFile5 interface [BITS],described, bits.ibackgroundcopyfile5, bits5_0/IBackgroundCopyFile5
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bits5_0.h
req.include-header: 
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
tech.root: 
req.typenames: BITS_FILE_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits5_0.h
api_name:
-	IBackgroundCopyFile5
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBackgroundCopyFile5 interface


## -description


Use this 
interface to get or set generic properties of BITS file transfers.

To get an 
<b>IBackgroundCopyFile5</b> interface pointer, call the <b>IBackgroundCopyFile::QueryInterface</b> method using __uuidof(IBackgroundCopyFile5) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBackgroundCopyFile5</b> interface inherits from <a href="https://msdn.microsoft.com/d404c4f8-cc97-4254-bca8-41bc359f0777">IBackgroundCopyFile4</a>. <b>IBackgroundCopyFile5</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBackgroundCopyFile5</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7afe4d11-f611-40ea-be94-7825f95576de">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of a generic BackgroundCopyFile property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a5809ef-e84f-4566-a5fa-fd63b1dfd15c">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a generic BackgroundCopyFile property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/facff24d-56a3-4a1f-a726-3442c17fe869">IBackgroundCopyFile2</a>



<a href="https://msdn.microsoft.com/5304f93a-993a-4327-9fdb-fb2ef1dafecb">IBackgroundCopyFile3</a>



<a href="https://msdn.microsoft.com/d404c4f8-cc97-4254-bca8-41bc359f0777">IBackgroundCopyFile4</a>
 

 

