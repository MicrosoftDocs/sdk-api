---
UID: NN:winsync.IProviderConverter
title: IProviderConverter (winsync.h)
author: windows-sdk-content
description: When implemented by a derived class, represents an object that can convert an ISyncProvider object to an IKnowledgeSyncProvider object.
old-location: winsync\iproviderconverter.htm
tech.root: winsync
ms.assetid: 67dc6290-00e8-457a-97be-efe8e731619d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IProviderConverter, IProviderConverter interface [Windows Sync], IProviderConverter interface [Windows Sync],described, winsync.iproviderconverter, winsync/IProviderConverter
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IProviderConverter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IProviderConverter interface


## -description


When implemented by a derived class, represents an object that can convert an <b>ISyncProvider</b> object to an <b>IKnowledgeSyncProvider</b> object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProviderConverter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProviderConverter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProviderConverter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bdb8b16-cda3-4f0d-b147-4dcfce81f592">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the <b>IProviderConverter</b> object with the <b>ISyncProvider</b> object to be converted.


</td>
</tr>
</table> 


## -remarks



<b>IProviderConverter</b> is typically implemented by the developer of the custom provider that it converts.




## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

